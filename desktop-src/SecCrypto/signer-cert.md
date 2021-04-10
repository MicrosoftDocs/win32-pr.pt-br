---
description: Especifica um certificado usado para assinar um documento. O certificado pode ser armazenado em um arquivo de certificado do fornecedor de software (SPC) ou em um repositório de certificados.
ms.assetid: 9a99ce98-237d-4223-ab3d-0576041038e3
title: Estrutura de SIGNER_CERT
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_CERT
api_type:
- NA
api_location: ''
ms.openlocfilehash: a14f955749e98ca34cda0be2c57a3d5c546afc41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171107"
---
# <a name="signer_cert-structure"></a>Estrutura do certificado do ASSINAnte \_

A estrutura de **\_ certificado do signatário** especifica um [*certificado*](../secgloss/c-gly.md) usado para assinar um documento. O certificado pode ser armazenado em um arquivo de [*certificado do fornecedor de software*](../secgloss/s-gly.md) (SPC) ou em um repositório de [*certificados*](../secgloss/c-gly.md).

> [!Note]  
> Essa estrutura não está definida em nenhum arquivo de cabeçalho. Para usar essa estrutura, você deve defini-la por conta própria, conforme mostrado neste tópico.

 

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _SIGNER_CERT {
  DWORD cbSize;
  DWORD dwCertChoice;
  union {
    LPCWSTR                pwszSpcFile;
    SIGNER_CERT_STORE_INFO *pCertStoreInfo;
    SIGNER_SPC_CHAIN_INFO  *pSpcChainInfo;
  };
  HWND  hwnd;
} SIGNER_CERT, *PSIGNER_CERT;
```



## <a name="members"></a>Membros

<dl> <dt>

**cbSize**
</dt> <dd>

O tamanho, em bytes, da estrutura.

</dd> <dt>

**dwCertChoice**
</dt> <dd>

Especifica como o certificado é armazenado. Esse membro pode ser um ou mais dos valores a seguir.



| Valor                                                                                                                                                                                                                                          | Significado                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIGNER_CERT_SPC_FILE"></span><span id="signer_cert_spc_file"></span><dl> <dt>**Signatário \_ \_ \_ Arquivo SPC do certificado**</dt> <dt>1</dt> </dl>    | O certificado é armazenado em um arquivo SPC. O membro **pwszSpcFile** contém o caminho e o nome do arquivo do SPC.<br/>                                                                                                                                                  |
| <span id="SIGNER_CERT_STORE"></span><span id="signer_cert_store"></span><dl> <dt>**Signatário \_ \_Repositório de certificados**</dt> <dt>2</dt> </dl>              | O certificado é armazenado em um repositório de certificados. O membro **pCertStoreInfo** contém um ponteiro para uma estrutura de informações de [**repositório de certificados de assinante \_ \_ \_**](signer-cert-store-info.md) que especifica o repositório de certificados no qual o certificado é armazenado.<br/>                 |
| <span id="SIGNER_CERT_SPC_CHAIN"></span><span id="signer_cert_spc_chain"></span><dl> <dt>**Signatário \_ \_ \_ Cadeia SPC do certificado**</dt> <dt>3</dt> </dl> | O certificado é armazenado em um arquivo SPC e está associado a uma cadeia de certificados. O membro **pSpcChainInfo** contém um ponteiro para uma estrutura de informações de cadeia do SPC de [**signatário \_ \_ \_**](signer-spc-chain-info.md) que contém as informações de cadeia para o certificado.<br/> |



 

</dd> <dt>

**pwszSpcFile**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres Unicode terminada em nulo que contém o caminho e o nome do arquivo do SPC no qual o certificado é armazenado. Esse membro só será usado se o membro **dwCertChoice** contiver o **\_ \_ \_ arquivo SPC do certificado do signatário**.

</dd> <dt>

**pCertStoreInfo**
</dt> <dd>

Um ponteiro para uma estrutura de [**\_ informações de repositório de certificados \_ \_ de assinante**](signer-cert-store-info.md) que especifica o repositório de certificados no qual o certificado é armazenado. Esse membro só será usado se o membro **dwCertChoice** contiver **\_ \_ repositório de certificados de assinante**.

</dd> <dt>

**pSpcChainInfo**
</dt> <dd>

Um ponteiro para uma estrutura de informações de cadeia do SPC de signatário que contém as informações de cadeia do certificado. [**\_ \_ \_**](signer-spc-chain-info.md) Esse membro só será usado se o membro **dwCertChoice** contiver uma **\_ \_ \_ cadeia SPC do certificado do assinante**.

</dd> <dt>

**HWND**
</dt> <dd>

O identificador da janela a ser usada como o proprietário de qualquer caixa de diálogo exibida. Esse membro não é usado no momento e é ignorado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SignerSign**](signersign.md)
</dt> <dt>

[**SignerSignEx**](signersignex.md)
</dt> </dl>

 

 
