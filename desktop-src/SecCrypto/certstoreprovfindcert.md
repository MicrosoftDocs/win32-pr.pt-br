---
description: Enumera ou localiza o primeiro ou o próximo certificado em um armazenamento externo que corresponde aos critérios especificados.
ms.assetid: 1129a372-4d7c-454e-969b-26a1d6037bc0
title: Função de retorno de chamada CertStoreProvFindCert
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFindCert
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: a50a53e819fcfd12ff490b4e6642536c01d9a49b4e9345e7713bf0eb08a0fac6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770015"
---
# <a name="certstoreprovfindcert-callback-function"></a>Função de retorno de chamada CertStoreProvFindCert

A função de retorno de **chamada CertStoreProvFindCert** enumera ou localiza o primeiro ou o próximo certificado em um repositório [*externo*](../secgloss/e-gly.md) que corresponde aos critérios especificados.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI CertStoreProvFindCert(
  _In_    HCERTSTOREPROV              hStoreProv,
  _In_    PCCERT_STORE_PROV_FIND_INFO pFindInfo,
  _In_    PCCERT_CONTEXT              pPrevCertContext,
  _In_    DWORD                       dwFlags,
  _Inout_ void                        **ppvStoreProvFindInfo,
  _Out_   PCCERT_CONTEXT              *ppProvCertContext
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hStoreProv* \[ Em\]
</dt> <dd>

**Alça HCERTSTOREPROV** para um repositório [*de certificados*](../secgloss/c-gly.md).

</dd> <dt>

*pFindInfo* \[ Em\]
</dt> <dd>

Um ponteiro para uma [**estrutura CERT \_ STORE \_ PROV FIND \_ \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) que contém todos os parâmetros passados para a [**função CertFindCertificateInStore.**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore)

</dd> <dt>

*pPrevCertContext* \[ Em\]
</dt> <dd>

Um ponteiro para um [**\_ CONTEXTO DE CERTIFICADO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) do certificado encontrado. Na primeira chamada para a função, esse parâmetro deve ser definido como **NULL.** Em chamadas subsequentes, ele deve ser definido como o ponteiro retornado no *parâmetro ppProvCertContext* na última chamada. Um ponteiro não **NULL** passado nesse parâmetro é liberado pela função de retorno de chamada.

</dd> <dt>

*dwFlags* \[ Em\]
</dt> <dd>

Quaisquer valores de sinalizador necessários.

</dd> <dt>

*ppvStoreProvFindInfo* \[ in, out\]
</dt> <dd>

Um ponteiro para um ponteiro para um buffer para retornar as informações do provedor de armazenamento. Opcionalmente, o retorno de chamada pode retornar um ponteiro para informações de busca internas neste parâmetro. Após a primeira chamada, esse parâmetro é definido como o ponteiro retornado pela chamada anterior para a função.

</dd> <dt>

*ppProvCertContext* \[ out\]
</dt> <dd>

Em uma busca bem-sucedida, um ponteiro para o certificado encontrado é retornado nesse parâmetro.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **TRUE** se a função for bem-sucedida **ou FALSE** se falhar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CONTEXTO DO \_ CERTIFICADO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[**INFORMAÇÕES \_ DE ENCONTRE O \_ PROV DO ARMAZENAMENTO DE \_ \_ CERTIFICADOS**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info)
</dt> <dt>

[**CertFindCertificateInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore)
</dt> </dl>

 

 
