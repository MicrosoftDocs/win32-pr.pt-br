---
description: Este tópico explica como registrar um Gerenciador de visualização associado a um determinado tipo de dados.
ms.assetid: 5f194d29-d09f-4426-a63e-911db65ce700
title: Como registrar um Gerenciador de visualização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5af9610de1822678521557fc20aa53f4e556e0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967892"
---
# <a name="how-to-register-a-preview-handler"></a>Como registrar um Gerenciador de visualização

Este tópico explica como registrar um Gerenciador de visualização associado a um determinado tipo de dados. Para fins de ilustração, os exemplos neste tópico usam um tipo de arquivo. xyz. O registro de um Gerenciador de visualização é um registro padrão baseado em associação de arquivo.

## <a name="instructions"></a>Instruções

### <a name="step-1"></a>Etapa 1:

Primeiro, uma extensão de nome de arquivo é associada a um ProgID. A entrada a seguir associa a subchave ProgID **xyzfile** com a extensão de nome de arquivo. xyz.

```
HKEY_CLASSES_ROOT
   .xyz
      (Default) = [REG_SZ] xyzfile
```

A subchave ProgID do **xyzfile** é armazenada com os outros ProgIDs, conforme mostrado aqui:

```
HKEY_CLASSES_ROOT
   xyzfile
```

Cada subchave ProgID do Gerenciador de visualização contém uma subchave chamada **shellex** que contém uma subchave *sempre* chamada **{8895b1c6-b41f-4c1c-a562-0d564250836f}**. A presença dessa subchave informa ao sistema que o manipulador é um Gerenciador de visualização.

O valor padrão da subchave **{8895b1c6-b41f-4c1c-a562-0d564250836f}** é o identificador de classe (CLSID) do seu manipulador. Um exemplo da subchave ProgID **xyzfile** é mostrado aqui, associando um manipulador de CLSID {ec3a629a-a47c-4245-bc78-b4b63d0e3154}.

```
HKEY_CLASSES_ROOT
   xyzfile
      shellex
         {8895b1c6-b41f-4c1c-a562-0d564250836f}
            (Default) = [REG_SZ] {ec3a629a-a47c-4245-bc78-b4b63d0e3154}
```

### <a name="step-2"></a>Etapa 2:

Em seguida, adicione a subchave sob **CLSID** para o seu Gerenciador de visualização. Um exemplo é mostrado aqui. Segue uma explicação das entradas individuais.

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

O valor padrão para sua subchave (aqui, **{ec3a629a-a47c-4245-bc78-b4b63d0e3154}**) não é obrigatório ou usado. No entanto, configurá-lo como uma cadeia de caracteres não-localada pode ajudá-lo a depurar problemas de registro.

O sinal de subtração (-101) no recurso. dll na entrada DisplayName existe por motivos herdados. A entrada de ícone, por outro lado, não requer um sinal de subtração.

O valor de AppID fornece uma referência à AppID do aplicativo associado à extensão de nome de arquivo (armazenada sob a ID do grupo de **classe de hKey \_ \_ raiz** \\ . O valor usado aqui — {6d2b5079-2f0b-48dd-ab7f-97cec514d30b} — é a ID da Prevhost.exe host substituto. os gerenciadores de visualização de 32 bits devem usar **AppID** {534A1E02-D58F-44f0-B58B-36CBED287C7C} quando instalados em sistemas operacionais de 64 bits.

As entradas na subchave **InprocServer32** incluem uma referência de volta à subchave ProgID da extensão de nome de arquivo, bem como uma entrada para um [VersionIndependentProgId](../com/versionindependentprogid.md).

### <a name="step-3"></a>Etapa 3:

Por fim, o Gerenciador de visualização deve ser adicionado à lista de todos os gerenciadores de visualização. Essa lista é usada como uma otimização pelo sistema para enumerar todos os gerenciadores de visualização registrados para fins de exibição. Novamente, o valor padrão não é necessário, ele simplesmente ajuda no processo de depuração.

> [!Note]  
> No Windows 7, se o aplicativo estiver instalado para todos os usuários do computador, use HKEY \_ local \_ Machine; se para apenas um usuário, use hKey \_ Current \_ User.

 

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

[Gerenciadores de visualização e host de visualização do Shell](preview-handlers.md)
</dt> <dt>

[Criando gerenciadores de visualização](building-preview-handlers.md)
</dt> <dt>

[Diretrizes do Gerenciador de visualização](preview-handler-guidelines.md)
</dt> </dl>

 

 
