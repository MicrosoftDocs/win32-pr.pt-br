---
description: Fornece a funcionalidade para assinar arquivos executáveis com uma assinatura digital Authenticode.
ms.assetid: e6d4e694-471f-4d30-983c-6bc5d631d99e
title: Objeto SignedCode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 08648c8b941874a6d1e1ed97d49f510694b998b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769272"
---
# <a name="signedcode-object"></a>Objeto SignedCode

\[O objeto **SignedCode** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use o PInvoke (serviços de invocação de plataforma) para chamar as funções [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md)e [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) da API do Win32 para assinar conteúdo com uma assinatura digital Authenticode. Para obter informações sobre PInvoke, consulte [tutorial de invocação de plataforma](https://msdn.microsoft.com/library/aa288468.aspx). O [.net e o CryptoAPI via p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.net e CryptoAPI via p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subseções de [estender a criptografia .NET com capicor e P/Invoke](/previous-versions/ms867087(v=msdn.10)) também podem ser úteis.\]

O objeto **SignedCode** fornece funcionalidade para assinar arquivos executáveis com uma assinatura digital Authenticode.

## <a name="when-to-use"></a>Quando usar

O objeto **SignedCode** é usado para executar as seguintes tarefas:

-   Assinar arquivos executáveis.
-   Arquivos executáveis de carimbo de data/hora.
-   Determine se a assinatura do arquivo executável é válida.
-   Defina ou recupere o caminho para o arquivo executável.
-   Recupere o signatário e a hora Stamper do arquivo executável.
-   Recupere uma coleção de certificados para o arquivo executável.
-   Recupere uma descrição ou a URL para a descrição do arquivo executável.

## <a name="members"></a>Membros

O objeto **SignedCode** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **SignedCode** tem esses métodos.



| Método                                    | Descrição                                                                                                                                                         |
|:------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Assine**](signedcode-sign.md)           | Cria uma assinatura digital Authenticode e assina o arquivo executável especificado na propriedade [**SignedCode. FileName**](signedcode-filename.md) .<br/>    |
| [**Timestamp**](signedcode-timestamp.md) | Cria uma assinatura de carimbo de data/hora Authenticode no arquivo executável assinado especificado na propriedade [**SignedCode. FileName**](signedcode-filename.md) .<br/> |
| [**Verificar**](signedcode-verify.md)       | Verifica a assinatura Authenticode no arquivo executável assinado especificado na propriedade [**SignedCode. FileName**](signedcode-filename.md) .<br/>          |



 

### <a name="properties"></a>Propriedades

O objeto **SignedCode** tem essas propriedades.



| Propriedade                                                       | Tipo de acesso           | Descrição                                                                                                                                |
|:---------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**Certificados**](signedcode-certificates.md)<br/>     | Somente leitura<br/>  | Uma coleção de [**certificados**](certificates.md) que contém todos os certificados no arquivo executável assinado.<br/>             |
| [**Descrição**](signedcode-description.md)<br/>       | Leitura/gravação<br/> | Uma cadeia de caracteres que contém uma descrição do arquivo executável assinado.<br/>                                                             |
| [**DescriptionURL**](signedcode-descriptionurl.md)<br/> | Leitura/gravação<br/> | Uma cadeia de caracteres que contém o endereço HTTP para uma descrição do arquivo executável assinado.<br/>                                         |
| [**Nome do arquivo**](signedcode-filename.md)<br/>             | Leitura/gravação<br/> | Uma cadeia de caracteres que contém o caminho para o arquivo de conteúdo que contém o arquivo executável.<br/> Essa é a propriedade padrão.<br/> |
| [**Signatário**](signedcode-signer.md)<br/>                 | Somente leitura<br/>  | Um objeto de [**signatário**](signer.md) que fornece acesso ao signatário do arquivo executável.<br/>                                    |
| [**Timestamper**](signedcode-timestamper.md)<br/>       | Somente leitura<br/>  | Um objeto de [**signatário**](signer.md) que fornece acesso ao Stamper de tempo do arquivo executável.<br/>                              |



 

## <a name="remarks"></a>Comentários

O objeto **SignedCode** pode ser criado e não é seguro para scripts. O ProgID do objeto **SignedCode** é CAPICOM. SignedCode. 1.

O arquivo executável deve ser de um tipo que possa ser assinado com a tecnologia Authenticode, por exemplo, arquivos que têm uma extensão de nome de arquivo. cab,. Cat,. exe,. dll,. vbs ou. ocx.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
