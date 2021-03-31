---
title: Instalação do manipulador de arquivos e fluxos
description: Instalação do manipulador de arquivos e fluxos
ms.assetid: 8d007ea4-b75a-4b3f-965f-8091fcd4cb2f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be94137df69ed35b57b1b8fbeb5c9640dd7636d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636934"
---
# <a name="file-and-stream-handler-installation"></a>Instalação do manipulador de arquivos e fluxos

A biblioteca AVIFile usa manipuladores de fluxo e arquivo instalados para ler e gravar arquivos AVI e fluxos. Um manipulador é instalado quando ele reside no diretório de sistema do Windows e o registro contém as seguintes informações necessárias para descrever e identificar um manipulador:

-   O identificador de classe de 16 bytes para o manipulador
-   Uma breve descrição do manipulador
-   O nome do arquivo que contém o manipulador
-   A extensão de arquivo que um manipulador de arquivo pode processar
-   Acesso a arquivos e outras propriedades associadas a um manipulador de arquivos
-   Códigos de quatro caracteres identificando os tipos de fluxo que um manipulador de fluxo pode processar

A biblioteca AVIFile consulta o registro de manipuladores que são externos a um aplicativo ao abrir arquivos e acessar fluxos. O resultado de uma consulta bem-sucedida retorna o FileName de um manipulador que pode processar o arquivo ou o tipo de fluxo especificado na consulta. O registro lista cada manipulador criando três entradas que têm o seguinte formato:


```C++
[HKEY_CLASSES_ROOT\Clsid\{00010023-0000-0000-C000-000000000046}] 
@="Wave File reader/writer" 
[HKEY_CLASSES_ROOT\Clsid\{00010023-0000-0000-C000- 
000000000046}\InprocServer32] 
@="wavefile.dll" 
"ThreadingModel"="Apartment" 
[HKEY_CLASSES_ROOT\Clsid\{00010023-0000-0000-C000- 
000000000046}\AVIFile] 
@="3" 
 
```



Essas entradas consistem nas seguintes partes.



| Parte                                   | Descrição                                                                                                                                                                              |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_raiz de classes hKey \_                    | Identifica a entrada raiz do registro.                                                                                                                                               |
| Clsid                                  | Identifica essa entrada como um identificador de classe.                                                                                                                                             |
| {00010023-0000-0000-C000-000000000046} | Especifica um identificador de interface (IID) ou identificador de classe. Esse valor é um identificador exclusivo de 16 bytes. (O identificador também pode ser referido como um GUID ou um UUID em outros manuais.) |
| Leitor/gravador de arquivo Wave                | Especifica uma cadeia de caracteres para descrever o manipulador. Essa cadeia de caracteres pode ser exibida em caixas de diálogo para selecionar manipuladores de fluxo e arquivo.                                                         |
| InProcServer32                         | Especifica o arquivo (neste exemplo, WAVEFILE.DLL) que pode ser carregado para lidar com essa classe.                                                                                              |
| AVIFile                                | Especifica as propriedades de um manipulador de arquivo. Neste exemplo, o manipulador pode ler e gravar em um arquivo AVI.                                                                              |



 

Um manipulador de arquivos pode ter uma ou mais de suas propriedades armazenadas no registro. As constantes a seguir identificam as propriedades atualmente associadas a um arquivo.



| Constante                        | Descrição                                                          |
|---------------------------------|----------------------------------------------------------------------|
| AVIFILEHANDLER \_ CANACCEPTNONRGB | Indica que um manipulador de arquivo pode processar dados de imagem diferentes de RGB. |
| AVIFILEHANDLER \_ CANread         | Indica que um manipulador de arquivo pode abrir um arquivo com acesso de leitura.      |
| AVIFILEHANDLER \_ CANWRITE        | Indica que um manipulador de arquivo pode abrir um arquivo com acesso de gravação.     |



 

Ao criar um manipulador de arquivo ou fluxo, você pode obter um novo identificador executando UUIDGEN.EXE. Sempre use UUIDGEN.EXE para criar um novo identificador. O número hexadecimal de 16 bytes criado por esse executável identificará exclusivamente seu manipulador.

A biblioteca AVIFile usa entradas adicionais no registro para identificar um identificador de classe com base na extensão de arquivo que um manipulador de arquivo pode processar ou um código de quatro caracteres que um arquivo ou manipulador de fluxo pode processar. Por exemplo, as entradas a seguir associam um identificador de classe à extensão de arquivo. WAV e o código de quatro caracteres "WAVE":


```C++
[HKEY_CLASSES_ROOT\AVIFile\Extensions\WAV] 
@="{00010023-0000-0000-C000-000000000046}" 
[HKEY_CLASSES_ROOT\AVIFile\RIFFHandlers\WAVE] 
@="{00010023-0000-0000-C000-000000000046}" 
 
```



Essas entradas consistem nas seguintes partes.



| Parte                                   | Descrição                                                                                       |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| \_raiz de classes hKey \_                    | Identifica a entrada raiz do registro.                                                        |
| AVIFile                                | Identifica essa entrada como uma entrada usada pelo AVIFile.                                                |
| Extensões                             | Especifica a extensão de arquivo (neste exemplo,. WAV) que um manipulador de arquivo pode processar.             |
| RIFFHandlers                           | Especifica o código de quatro caracteres (neste exemplo, "WAVE") que um arquivo ou manipulador de fluxo pode processar. |
| {00010023-0000-0000-C000-000000000046} | Especifica um identificador de interface (IID) ou identificador de classe.                                      |



 

Se você distribuir o fluxo ou o manipulador de arquivos sem um aplicativo de instalação para instalá-lo no sistema do usuário, deverá incluir um. O arquivo REG para que o usuário possa instalar o manipulador. O usuário usará o editor do registro para criar entradas de registro para o seu manipulador de fluxo ou arquivo.

O exemplo a seguir mostra o conteúdo de um típico. Arquivo REG. A primeira entrada no exemplo a seguir é a cadeia de caracteres descritiva para o manipulador. A segunda entrada identifica o arquivo que contém o manipulador. A terceira entrada identifica as propriedades do manipulador de arquivo (nesse caso, acesso somente leitura aos arquivos). A quarta entrada associa o tipo de arquivo que o manipulador processa (nesse caso, arquivos com um. Extensão de nome de arquivo JPG) com o identificador de classe.


```C++
[HKEY_CLASSES_ROOT\Clsid\{5C2B8200-E2C8-1068-B1CA-6066188C6002}] 
@="JFIF (JPEG) Files" 
[HKEY_CLASSES_ROOT\Clsid\{5C2B8200-E2C8-1068-B1CA-6066188C6002}]\InprocServer32] 
@="jfiffile.dll" 
[HKEY_CLASSES_ROOT\AVIFile\Extensions\JPG] 
@="{5C2B8200-E2C8-1068-B1CA-6066188C6002}" 
 
```



Ao criar esse arquivo, salve-o com um. REG Extension para identificá-lo como um arquivo de atualização para o registro. Além disso, substitua um IID exclusivo pelo código de 16 bytes usado no exemplo.

 

 




