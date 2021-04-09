---
description: Especifica um SPC (certificado do fornecedor de software) e uma cadeia de certificados usados para assinar um documento.
ms.assetid: b65b4129-df92-410c-b372-b0c004f8bb03
title: Estrutura de SIGNER_SPC_CHAIN_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_SPC_CHAIN_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 60279a60e6cdfbf43a1e2d9c45735b885d97a055
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091621"
---
# <a name="signer_spc_chain_info-structure"></a>\_Estrutura de \_ informações da cadeia do SPC do signatário \_

A estrutura de **\_ \_ \_ informações da cadeia SPC do signatário** especifica um certificado do fornecedor de [*software*](../secgloss/s-gly.md) (SPC) e uma cadeia de certificados usados para assinar um documento.

> [!Note]  
> Essa estrutura não está definida em nenhum arquivo de cabeçalho. Para usar essa estrutura, você deve defini-la por conta própria, conforme mostrado neste tópico.

 

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _SIGNER_SPC_CHAIN_INFO {
  DWORD      cbSize;
  LPCWSTR    pwszSpcFile;
  DWORD      dwCertPolicy;
  HCERTSTORE hCertStore;
} SIGNER_SPC_CHAIN_INFO, *PSIGNER_SPC_CHAIN_INFO;
```



## <a name="members"></a>Membros

<dl> <dt>

**cbSize**
</dt> <dd>

O tamanho, em bytes, da estrutura.

</dd> <dt>

**pwszSpcFile**
</dt> <dd>

O nome do arquivo SPC a ser usado para assinar um documento.

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

 

 
