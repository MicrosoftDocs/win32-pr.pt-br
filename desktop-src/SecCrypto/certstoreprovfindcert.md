---
description: Enumera ou localiza o primeiro certificado ou próximo em um repositório externo que corresponda aos critérios especificados.
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
ms.openlocfilehash: 09701991d6b192d27f921642bfc960df819f9140
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297064"
---
# <a name="certstoreprovfindcert-callback-function"></a>Função de retorno de chamada CertStoreProvFindCert

A função de retorno de chamada **CertStoreProvFindCert** enumera ou localiza o primeiro ou próximo certificado em um [*repositório externo*](../secgloss/e-gly.md) que corresponde aos critérios especificados.

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

*hStoreProv* \[ no\]
</dt> <dd>

Identificador de **HCERTSTOREPROV** para um [*repositório de certificados*](../secgloss/c-gly.md).

</dd> <dt>

*pFindInfo* \[ no\]
</dt> <dd>

Um ponteiro para uma [**loja de certificados \_ \_ Prov \_ encontrar \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) a estrutura de informações contendo todos os parâmetros passados para a função [**CertFindCertificateInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore) .

</dd> <dt>

*pPrevCertContext* \[ no\]
</dt> <dd>

Um ponteiro para um [**\_ contexto CERT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) do certificado encontrado. Na primeira chamada para a função, esse parâmetro deve ser definido como **NULL**. Em chamadas subsequentes, ele deve ser definido como o ponteiro retornado no parâmetro *ppProvCertContext* na última chamada. Um ponteiro não **nulo** passado nesse parâmetro é liberado pela função de retorno de chamada.

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Quaisquer valores de sinalizador necessários.

</dd> <dt>

*ppvStoreProvFindInfo* \[ entrada, saída\]
</dt> <dd>

Um ponteiro para um ponteiro para um buffer para retornar as informações do provedor de repositório. Opcionalmente, o retorno de chamada pode retornar um ponteiro para informações de localização internas nesse parâmetro. Após a primeira chamada, esse parâmetro é definido como o ponteiro retornado pela chamada anterior para a função.

</dd> <dt>

*ppProvCertContext* \[ fora\]
</dt> <dd>

Em uma localização bem-sucedida, um ponteiro para o certificado encontrado é retornado nesse parâmetro.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará **true** se a função for bem-sucedida ou **false** se falhar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**contexto do certificado \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[**informações de localização do repositório de certificados \_ \_ Prov \_ \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info)
</dt> <dt>

[**CertFindCertificateInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore)
</dt> </dl>

 

 
