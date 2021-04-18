---
description: Especifica o repositório de certificados usado para assinar um documento.
ms.assetid: aabad010-6fa3-4677-bd73-b8c52d68dbc8
title: Estrutura de SIGNER_CERT_STORE_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_CERT_STORE_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 197bd4855a7d2afec4c0b23662365e5f9197e302
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105767818"
---
# <a name="signer_cert_store_info-structure"></a>\_Estrutura de \_ informações do repositório de certificados do assinante \_

A estrutura de informações do repositório de certificados do signatário especifica o repositório de certificados usado para assinar um documento. **\_ \_ \_**

> [!Note]  
> Essa estrutura não está definida em nenhum arquivo de cabeçalho. Para usar essa estrutura, você deve defini-la por conta própria, conforme mostrado neste tópico.

 

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _SIGNER_CERT_STORE_INFO {
  DWORD          cbSize;
  PCCERT_CONTEXT pSigningCert;
  DWORD          dwCertPolicy;
  HCERTSTORE     hCertStore;
} SIGNER_CERT_STORE_INFO, *PSIGNER_CERT_STORE_INFO;
```



## <a name="members"></a>Membros

<dl> <dt>

**cbSize**
</dt> <dd>

O tamanho, em bytes, da estrutura.

</dd> <dt>

**pSigningCert**
</dt> <dd>

Um ponteiro para uma estrutura de [**\_ contexto**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) de certificado para o certificado de autenticação.

</dd> <dt>

**dwCertPolicy**
</dt> <dd>

Especifica como os certificados são adicionados à assinatura. Para localizar a cadeia de certificados, as lojas MY, AC, ROOT e SPC, além da loja especificada pelo membro **HCERTSTORE** , são verificadas. Esse membro pode ser um ou mais dos valores a seguir.



| Valor                                                                                                                                                                                                                                                                                   | Significado                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIGNER_CERT_POLICY_CHAIN"></span><span id="signer_cert_policy_chain"></span><dl> <dt>**Signatário \_ \_ \_ Grupo de políticas de CERT**</dt> . <dt>2 (0x2)</dt> </dl>                           | Adicione somente certificados na cadeia de certificados.<br/>                                                                                                                                |
| <span id="SIGNER_CERT_POLICY_CHAIN_NO_ROOT"></span><span id="signer_cert_policy_chain_no_root"></span><dl> <dt>**Signatário \_ Cadeia de política de certificado \_ \_ \_ sem \_ raiz**</dt> <dt>8 (0x8)</dt> </dl> | Adicione somente certificados na cadeia de certificados, excluindo o certificado raiz.<br/>                                                                                                |
| <span id="SIGNER_CERT_POLICY_STORE"></span><span id="signer_cert_policy_store"></span><dl> <dt>**Signatário \_ \_ \_ Repositório de política de certificado**</dt> <dt>1 (0x1)</dt> </dl>                           | Adicione todos os certificados no repositório especificado pelo membro **HCERTSTORE** . Esse sinalizador pode ser uma combinação bit-a-**ou** com qualquer um dos outros valores possíveis para esse membro.<br/> |



 

</dd> <dt>

**hCertStore**
</dt> <dd>

Opcional. Um identificador para um repositório de certificados adicional.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**certificado do ASSINAnte \_**](signer-cert.md)
</dt> </dl>

 

 




