---
description: Um valor de registro pode armazenar dados em vários formatos.
ms.assetid: 5fd828d6-4d62-4823-a2f1-15782b5cd28c
title: Tipos de valor do registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adc653e69c514bc77323704485e88f0a57eebaae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828680"
---
# <a name="registry-value-types"></a>Tipos de valor do registro

Um valor de registro pode armazenar dados em vários formatos. Ao armazenar dados em um valor de registro, por exemplo, chamando a função [**RegSetValueEx**](/windows/desktop/api/Winreg/nf-winreg-regsetvalueexa) , você pode especificar um dos valores a seguir para indicar o tipo de dados que estão sendo armazenados. Quando você recupera um valor de registro, funções como [**RegQueryValueEx**](/windows/desktop/api/Winreg/nf-winreg-regqueryvalueexa) usam esses valores para indicar o tipo de dados recuperados.

Os seguintes tipos de valor de registro são definidos em Winnt. h.



| Valor                                 | Tipo                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_binário reg<br/>                | Dados binários em qualquer formulário.<br/>                                                                                                                                                                                                                                                                                                                                                                                                     |
| REG \_ DWORD<br/>                 | Um número de 32 bits.<br/>                                                                                                                                                                                                                                                                                                                                                                                                             |
| REG \_ DWORD de valor \_ pequeno \_<br/> | Um número de 32 bits no formato little-endian.<br/> O Windows foi projetado para ser executado em arquiteturas de computador little-endian. Portanto, esse valor é definido como REG \_ DWORD nos arquivos de cabeçalho do Windows.<br/>                                                                                                                                                                                                                          |
| REG \_ DWORD \_ Big \_ ENDIAN<br/>    | Um número de 32 bits no formato big-endian.<br/> Alguns sistemas UNIX oferecem suporte a arquiteturas big-endian.<br/>                                                                                                                                                                                                                                                                                                                         |
| REG \_ expande \_ sz<br/>            | Uma cadeia de caracteres terminada em nulo que contém referências não expandidas a variáveis de ambiente (por exemplo, "% PATH%"). Será uma cadeia de caracteres Unicode ou ANSI, dependendo se você usar as funções Unicode ou ANSI. Para expandir as referências de variáveis de ambiente, use a função [**ExpandEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-expandenvironmentstringsa) .<br/>                                                                                 |
| \_link reg<br/>                  | Uma cadeia de caracteres Unicode terminada em nulo que contém o caminho de destino de um link simbólico que foi criado chamando a função [**RegCreateKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeyexa) com a \_ opção reg \_ criar \_ link.<br/>                                                                                                                                                                                                                          |
| REG \_ multi \_ sz<br/>             | Uma sequência de cadeias de caracteres terminadas em nulo, terminadas por uma cadeia de caracteres vazia ( \\ 0).<br/> A seguir, é mostrado um exemplo:<br/> *Seqüência1* \\ 0 *seqüência2* \\ 0 *String3* \\ 0 *últimastring* \\ 0 \\ 0<br/> O primeiro \\ 0 termina a primeira cadeia de caracteres, o segundo para o último \\ 0 encerra a última cadeia de caracteres e o final \\ 0 termina a sequência. Observe que o terminador final deve ser acrescentado ao comprimento da cadeia de caracteres.<br/> |
| REG \_ None<br/>                  | Nenhum tipo de valor definido.<br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| REG \_ QWORD<br/>                 | Um número de 64 bits.<br/>                                                                                                                                                                                                                                                                                                                                                                                                             |
| REG \_ QWORD \_ Little \_ ENDIAN<br/> | Um número de 64 bits no formato little-endian.<br/> O Windows foi projetado para ser executado em arquiteturas de computador little-endian. Portanto, esse valor é definido como REG \_ QWORD nos arquivos de cabeçalho do Windows.<br/>                                                                                                                                                                                                                          |
| REG \_ sz<br/>                    | Uma cadeia de caracteres terminada em nulo. Isso será uma cadeia de caracteres Unicode ou ANSI, dependendo se você usar as funções Unicode ou ANSI.<br/>                                                                                                                                                                                                                                                                                       |



 

## <a name="string-values"></a>Valores de cadeia de caracteres

Se os dados tiverem o \_ tipo reg sz, Reg \_ multi \_ sz ou reg \_ expandem \_ sz, a cadeia de caracteres poderá não ter sido armazenada com os caracteres nulos de encerramento corretos. Portanto, ao ler uma cadeia de caracteres do registro, você deve garantir que a cadeia de caracteres seja encerrada corretamente antes de usá-la; caso contrário, ele pode substituir um buffer. (Observe que REG \_ As \_ cadeias de caracteres de vários sz devem ter duas terminações nulas.)

Ao gravar uma cadeia de caracteres no registro, você deve especificar o comprimento da cadeia de caracteres, incluindo o caractere nulo de terminação ( \\ 0). Um erro comum é usar a função **strlen** para determinar o comprimento da cadeia de caracteres, mas para esquecer que **strlen** retorna apenas o número de caracteres na cadeia de caracteres, não incluindo o nulo de terminação. Portanto, o comprimento da cadeia de caracteres deve ser calculado da seguinte maneira: `strlen( string ) + 1`

Uma \_ \_ cadeia de caracteres reg multi sz termina com uma cadeia de caracteres de comprimento 0. Portanto, não é possível incluir uma cadeia de caracteres de comprimento zero na sequência. Uma sequência vazia seria definida da seguinte maneira: \\ 0.

O exemplo a seguir percorre uma \_ cadeia de caracteres reg multi \_ sz.


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>

void SampleSzz(PTSTR pszz)
{
   _tprintf(_TEXT("\tBegin multi-sz string\n"));
   while (*pszz) 
   {
      _tprintf(_TEXT("\t\t%s\n"), pszz);
      pszz = pszz + _tcslen(pszz) + 1;
   }
   _tprintf(_TEXT("\tEnd multi-sz\n"));
}

int __cdecl main(int argc, char **argv)
{
   // Because the compiler adds a \0 at the end of quoted strings, 
   // there are two \0 terminators at the end. 

   _tprintf(_TEXT("Conventional multi-sz string:\n"));  
   SampleSzz(_TEXT("String1\0String2\0String3\0LastString\0"));

   _tprintf(_TEXT("\nTest case with no strings:\n"));  
   SampleSzz(_TEXT(""));

   return 0;
}
```



## <a name="byte-formats"></a>Formatos de byte

No *formato little-endian*, um valor de byte múltiplo é armazenado na memória do byte mais baixo (o "pequeno fim") para o byte mais alto. Por exemplo, o valor 0x12345678 é armazenado como (0x78 0x56 0x34 0x12) no formato little-endian.

No *formato big endian*, um valor de byte múltiplo é armazenado na memória do byte mais alto (o "grande fim") para o byte mais baixo. Por exemplo, o valor 0x12345678 é armazenado como (0x12 0x34 0x56 0x78) no formato big endian.

 

