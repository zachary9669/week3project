# week3project1

## Project Domain ideas
recipe organizer 
-make it interactive; store, organize, and set a timer…
-input ingredients and output the possible menu options

API: https://developer.edamam.com/edamam-docs-recipe-api 

package api;

import entity.Grade;
import entity.Team;
import okhttp3.*;
import org.json.JSONArray;
import org.json.JSONException;
import org.json.JSONObject;

import java.io.IOException;
import java.util.Arrays;

public class MongoGradeDB implements GradeDB {
    private static final String API_URL = "https://developer.edamam.com/edamam-docs-recipe-api";
    // load API_TOKEN from env variable.
    private static final String API_TOKEN = System.getenv("API_TOKEN");

    public static String getApiToken() {
        return API_TOKEN;
