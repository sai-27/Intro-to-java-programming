

public class Matrix {
	private double[][] matrix;
	private final int NUMROW;
	private final int NUMCOL;
	
	
	public Matrix(double[][] m) 
	{	
		matrix = m;
		NUMCOL = matrix[0].length;
		NUMROW = matrix.length;
	}
	
	
	public String toString() 
	{
		String returnString = "";
		returnString += (NUMCOL + "x" + NUMROW + "\n[");
		
		for (int rows = 0; rows < NUMROW; rows++)
		{
			for (int columns = 0; columns < NUMCOL; columns++)
			{
				returnString += matrix[rows][columns];
				
				if (columns + 1 != NUMCOL)
				{
					returnString += ", ";
				}
			} // end for 
			if (rows + 1 != NUMROW)
			{
				returnString += "\n ";
			}
		} // end for 
		
		returnString += "]";
		
		return returnString;
	}
	
	
	
	public Matrix transposeMatrix() 
	{
		// returns a new matrix 
		
		double[][] newArray = new double[NUMCOL][NUMROW];
		
		for (int columns = 0; columns < NUMCOL; columns++)
		{
			for (int rows = 0; rows < NUMROW; rows++)
			{
				newArray[columns][rows] = matrix[rows][columns];
			}
		}
		
		return new Matrix(newArray);
		
	}
	
	
	
	public Matrix getUpperDiagonal() 
	{
		double[][] newArray = new double[NUMROW][NUMCOL];
		
		for (int rows = 0; rows < NUMROW; rows++)
		{
			for (int columns = 0; columns < NUMCOL; columns++)
			{
				newArray[rows][columns] = matrix[rows][columns];
				if (columns > rows)
				{
					newArray[rows][columns] = 0;
				}
			}
		} // end for 
		
		return new Matrix(newArray);
	}
	
	
	
	public Matrix getLowerDiagonal() 
	{
		double[][] newArray = new double[NUMROW][NUMCOL];
		
		for (int rows = 0; rows < NUMROW; rows++)
		{
			for (int columns = 0; columns < NUMCOL; columns++)
			{
				newArray[rows][columns] = matrix[rows][columns];
				if (columns < rows)
				{
					newArray[rows][columns] = 0;
				}
			}
		} // end for 
		
		return new Matrix(newArray);
	}
	
	
	
	public Matrix getDiagonal ()
	{
		double[][] newArray = new double[NUMROW][NUMCOL];
		
		for (int rows = 0; rows < NUMROW; rows++)
		{
			for (int columns = 0; columns < NUMCOL; columns++)
			{
				newArray[rows][columns] = matrix[rows][columns];
				if (columns != rows)
				{
					newArray[rows][columns] = 0;
				}
			}
		} // end for 
		
		return new Matrix(newArray);
	}
	
	
	
	public Matrix getAntiDiagonal ()
	{
		double[][] newArray = new double[NUMROW][NUMCOL];
		
		for (int rows = 0; rows < NUMROW; rows++)
		{
			for (int columns = 0; columns < NUMCOL; columns++)
			{
				newArray[rows][columns] = matrix[rows][columns];
				if (columns == rows)
				{
					newArray[rows][columns] = 0;
				}
			}
		} // end for 
		
		return new Matrix(newArray);
	}
	
	
	
	public boolean isSquareMatrix() 
	{
		if (NUMROW == NUMCOL)
		{
			return true;
		}
		else
		{
			return false;
		}
	}
	
	
	
	public boolean isIdentityMatrix () 
	{
		
		double[][] identMat = new double[NUMROW][NUMCOL];
		
		if (NUMROW != NUMCOL)
		{
			return false;
		}
		
		for (int rows = 0; rows < NUMROW; rows++)
		{
			for (int columns = 0; columns < NUMCOL; columns++)
			{
				identMat[rows][columns] = matrix[rows][columns];
				if ( (!(columns == rows && identMat[rows][columns] == 1)) && (!(columns != rows && identMat[rows][columns] == -0)) )
				{
					return false;
				}
			}
		}  
			
		return true;
	}
	
	
	
	public boolean isEqual (Matrix m) 
	{
		if (NUMROW != m.NUMROW || NUMCOL != m.NUMCOL) // if the rows and columns are not equal
		{
			return false; 
		}
		else 
		{
			for (int row = 0; row < NUMROW; row++)
			{
				for (int column = 0; column < NUMCOL; column++)
				{
					if (matrix[row][column] != m.matrix[row][column])
					{
						return false;
					}
				}
			} 
			
			return true; 
		} 
		
		
	}
	
	
	
	public static void main(String[] args) 
	{
		double[][] twoDarray = {{1,4,2,3},{2,1,7,3},{9,3,0,1},{3,6,2,1}};
		double[][] sameArray = {{1,4,2,3},{2,1,7,3},{9,3,0,1},{3,6,2,1}};
		Matrix mat = new Matrix(twoDarray);
		Matrix sameMat = new Matrix(sameArray);
		
		System.out.println("This is the original Matrix.");
		System.out.println(mat.toString());
		
		System.out.println("This is the the transposed Matrix.");
		System.out.println(mat.transposeMatrix().toString());
		
		Matrix upperDiagnol = mat.getUpperDiagonal();
		Matrix lowerDiagnol = mat.getLowerDiagonal();
		
		System.out.println("Diagnol Lower Matrix");
		System.out.println(lowerDiagnol.toString());
		
		System.out.println("Diagnol Upper Matrix");
		System.out.println(upperDiagnol.toString());
		
		System.out.println("Is diagnol?:");
		System.out.println(mat.getDiagonal().toString());
		
		System.out.println("Anti-diagnol Matrix");
		System.out.println(mat.getAntiDiagonal().toString());
		
		System.out.println("Is identity matrix?:");
		System.out.println(mat.isIdentityMatrix());
		
		System.out.println("Are the two matrix identical?:");
		System.out.println(mat.isEqual(sameMat));
		
	}
	
	
}
