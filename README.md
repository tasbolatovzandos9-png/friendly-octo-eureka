import java.security.MessageDigest;
import java.security.NoSuchAlgorithmException;

public class Main {
    public static void main(String[] args) throws NoSuchAlgorithmException {

        String text = "Zhandos";

        MessageDigest md = MessageDigest.getInstance("MD5");
        byte[] hash = md.digest(text.getBytes());

        StringBuilder result = new StringBuilder();

        for (byte b : hash) {
            result.append(String.format("%02x", b));
        }

        System.out.println("MD5: " + result);
    }
}
