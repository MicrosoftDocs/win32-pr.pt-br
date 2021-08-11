---
description: Este tópico explica como registrar um manipulador de visualização associado a um determinado tipo de dados.
ms.assetid: 5f194d29-d09f-4426-a63e-911db65ce700
title: Como registrar um manipulador de visualização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e1879261750609015acee2ccea1bc6f48f82df78ac7c18cbb2f46fa493c4e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118223435"
---
# <a name="how-to-register-a-preview-handler"></a>Como registrar um manipulador de visualização

Este tópico explica como registrar um manipulador de visualização associado a um determinado tipo de dados. Para fins de ilustração, os exemplos neste tópico usam um tipo de arquivo .xyz. O registro de um manipulador de visualização é um registro padrão baseado em associação de arquivo.

## <a name="instructions"></a>Instruções

### <a name="step-1"></a>Etapa 1:

Primeiro, uma extensão de nome de arquivo é associada a um ProgID. A entrada a seguir associa a sub-chave **xyzfile** ProgID à extensão de nome de arquivo .xyz.

```
HKEY_CLASSES_ROOT
   .xyz
      (Default) = [REG_SZ] xyzfile
```

A **sub-chave xyzfile** ProgID é armazenada com os outros ProgIDs, conforme mostrado aqui:

```
HKEY_CLASSES_ROOT
   xyzfile
```

Cada subkey do manipulador de visualização ProgID contém  uma sub-chave chamada **shellex** que contém uma sub-chave sempre chamada **{8895b1c6-b41f-4c1c-a562-0d564250836f}.** A presença dessa sub-chave informa ao sistema que o manipulador é um manipulador de visualização.

O valor padrão da subkey **{8895b1c6-b41f-4c1c-a562-0d564250836f}** é o CLSID (identificador de classe) do manipulador. Um exemplo da sub-chave **xyzfile** ProgID é mostrado aqui, associando um manipulador de CLSID {ec3a629a-a47c-4245-bc78-b4b63d0e3154}.

```
HKEY_CLASSES_ROOT
   xyzfile
      shellex
         {8895b1c6-b41f-4c1c-a562-0d564250836f}
            (Default) = [REG_SZ] {ec3a629a-a47c-4245-bc78-b4b63d0e3154}
```

### <a name="step-2"></a>Etapa 2:

Em seguida, adicione a sub-chave em **CLSID para** o manipulador de visualização. Um exemplo é mostrado aqui. Segue uma explicação das entradas individuais.

```
HKEY_CLASSES_ROOT
   CLSID
      {ec3a629a-a47c-4245-bc78-b4b63d0e3154}
         (Default) = [REG_SZ] Fabricam XYZ Preview Handler
         DisplayName = [REG_SZ] @myhandler.dll,-101
         Icon = [REG_SZ] myhandler.dll,201
         AppID = [REG_SZ] {6d2b5079-2f0b-48dd-ab7f-97cec514d30b}
         InprocServer32
            (Default) = [REG_EXPAND_SZ] %ProgramFiles%\Fabricam\myhandler.dll
            ThreadingModel = [REG_SZ] Apartment
            ProgID = [REG_SZ] xyzfile
            VersionIndependentProgID = [REG_SZ] Version IndependentProgID
```

O valor padrão da sub-chave (aqui, **{ec3a629a-a47c-4245-bc78-b4b63d0e3154}**) não é necessário nem usado. No entanto, defini-lo como uma cadeia de caracteres não localizada pode ajudá-lo a depurar problemas de registro.

O sinal de subtração (-101) no .dll na entrada DisplayName existe por motivos herddos. A entrada Ícone, por outro lado, não requer um sinal de subtração.

O valor AppID fornece uma referência à AppID do aplicativo associado à extensão de nome de arquivo (armazenada em **HKEY \_ CLASSES \_ ROOT** \\ **APPID**. O valor usado aqui —{6d2b5079-2f0b-48dd-ab7f-97cec514d30b}— é a ID do host substituto do Prevhost.exe. Manipuladores de visualização de 32 bits devem usar **AppID** {534A1E02-D58F-44f0-B58B-36CBED287C7C} quando instalados em sistemas operacionais de 64 bits.

As entradas na sub-chave **InprocServer32** incluem uma referência à subkey ProgID da extensão de nome de arquivo, bem como uma entrada para [um VersionIndependentProgID](../com/versionindependentprogid.md).

### <a name="step-3"></a>Etapa 3:

Por fim, o manipulador de visualização deve ser adicionado à lista de todos os manipuladores de visualização. Essa lista é usada como uma otimização pelo sistema para enumerar todos os manipuladores de visualização registrados para fins de exibição. Novamente, o valor padrão não é necessário, ele simplesmente ajuda no processo de depuração.

> [!Note]  
> No Windows 7, se o aplicativo estiver instalado para todos os usuários do computador, use HKEY LOCAL MACHINE; se para apenas um \_ \_ usuário, use HKEY \_ CURRENT \_ USER.

 

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               PreviewHandlers
                  {ec3a629a-a47c-4245-bc78-b4b63d0e3154}
                     (Default) = [REG_SZ] Fabricam XYZ Preview Handler
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Manipuladores de visualização e host de visualização do Shell](preview-handlers.md)
</dt> <dt>

[Criando manipuladores de visualização](building-preview-handlers.md)
</dt> <dt>

[Diretrizes do manipulador de visualização](preview-handler-guidelines.md)
</dt> </dl>

 

 
