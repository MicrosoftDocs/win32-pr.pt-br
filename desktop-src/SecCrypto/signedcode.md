---
description: Fornece funcionalidade para assinar arquivos executáveis com uma assinatura digital Authenticode.
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
ms.openlocfilehash: e119a639af7cb6459e8e6ec8ae6416f9d067c56e8f81560fedc385abd518b840
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118899335"
---
# <a name="signedcode-object"></a>Objeto SignedCode

\[O **objeto SignedCode** está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Em vez disso, use os Serviços de Invocação de Plataforma (PInvoke) para chamar as funções [**SignerSignEx,**](signersignex.md) [**SignerTimeStampEx**](signertimestampex.md)e [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) para assinar conteúdo com uma assinatura digital Authenticode. Para obter informações sobre o PInvoke, consulte [Tutorial de invocação de plataforma.](https://msdn.microsoft.com/library/aa288468.aspx) O .NET e a CryptoAPI por meio de [P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) Parte 1 e .NET e CryptoAPI por meio de [P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subseções da parte 2 de Estender a criptografia do .NET com [CAPICOM e P/Invoke](/previous-versions/ms867087(v=msdn.10)) também podem ser úteis.\]

O **objeto SignedCode** fornece funcionalidade para assinar arquivos executáveis com uma assinatura digital Authenticode.

## <a name="when-to-use"></a>Quando usar

O **objeto SignedCode** é usado para executar as seguintes tarefas:

-   Assinar arquivos executáveis.
-   Arquivos executáveis de carimbo de data/hora.
-   Determine se a assinatura do arquivo executável é válida.
-   Definir ou recuperar o caminho para o arquivo executável.
-   Recupere o signante e o carimbo de data/hora do arquivo executável.
-   Recupere uma coleção de certificados para o arquivo executável.
-   Recupere uma descrição ou a URL para a descrição do arquivo executável.

## <a name="members"></a>Membros

O **objeto SignedCode** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O **objeto SignedCode** tem esses métodos.



| Método                                    | Descrição                                                                                                                                                         |
|:------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Sinal**](signedcode-sign.md)           | Cria uma assinatura digital Authenticode e assina o arquivo executável especificado na [**propriedade SignedCode.FileName.**](signedcode-filename.md)<br/>    |
| [**Timestamp**](signedcode-timestamp.md) | Cria uma assinatura de carimbo de data/hora Authenticode no arquivo executável assinado especificado na [**propriedade SignedCode.FileName.**](signedcode-filename.md)<br/> |
| [**Verificar**](signedcode-verify.md)       | Verifica a assinatura Authenticode no arquivo executável assinado especificado na [**propriedade SignedCode.FileName.**](signedcode-filename.md)<br/>          |



 

### <a name="properties"></a>Propriedades

O **objeto SignedCode** tem essas propriedades.



| Propriedade                                                       | Tipo de acesso           | Descrição                                                                                                                                |
|:---------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**Certificados**](signedcode-certificates.md)<br/>     | Somente leitura<br/>  | Uma [**coleção de Certificados**](certificates.md) que contém todos os certificados no arquivo executável assinado.<br/>             |
| [**Descrição**](signedcode-description.md)<br/>       | Leitura/gravação<br/> | Uma cadeia de caracteres que contém uma descrição do arquivo executável assinado.<br/>                                                             |
| [**Descriptionurl**](signedcode-descriptionurl.md)<br/> | Leitura/gravação<br/> | Uma cadeia de caracteres que contém o endereço HTTP para uma descrição do arquivo executável assinado.<br/>                                         |
| [**Filename**](signedcode-filename.md)<br/>             | Leitura/gravação<br/> | Uma cadeia de caracteres que contém o caminho para o arquivo de conteúdo que contém o arquivo executável.<br/> Essa é a propriedade padrão.<br/> |
| [**Signatário**](signedcode-signer.md)<br/>                 | Somente leitura<br/>  | Um [**objeto Signer**](signer.md) que fornece acesso ao signante do arquivo executável.<br/>                                    |
| [**Timestamper**](signedcode-timestamper.md)<br/>       | Somente leitura<br/>  | Um [**objeto Signer**](signer.md) que fornece acesso ao carimbo de data/hora do arquivo executável.<br/>                              |



 

## <a name="remarks"></a>Comentários

O **objeto SignedCode** pode ser criado e não é seguro para scripts. O ProgID para o **objeto SignedCode** é CAPICOM. SignedCode.1.

O arquivo executável deve ser de um tipo que pode ser assinado com a tecnologia Authenticode, por exemplo, arquivos que têm uma extensão de nome de arquivo de .cab, .cat, .exe, .dll, .vbs ou .ocx.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2.0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
