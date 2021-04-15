---
description: Enumera ou localiza a primeira ou a próxima CRL em um repositório externo que corresponde aos critérios especificados.
ms.assetid: caf218f5-f379-4cb6-bb4b-4767b846d45c
title: Função de retorno de chamada CertStoreProvFindCRL
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFindCRL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: b20b7a4b677356e59be9f2f6df47b260c12d2f64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506080"
---
# <a name="certstoreprovfindcrl-callback-function"></a>Função de retorno de chamada CertStoreProvFindCRL

A função de retorno de chamada **CertStoreProvFindCRL** enumera ou localiza a primeira ou a próxima [*CRL*](../secgloss/c-gly.md) em um [*repositório*](../secgloss/e-gly.md) externo que corresponde aos critérios especificados.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI CertStoreProvFindCRL(
  _In_    HCERTSTOREPROV              hStoreProv,
  _In_    PCCERT_STORE_PROV_FIND_INFO pFindInfo,
  _In_    PCCRL_CONTEXT               pPrevCrlContext,
  _In_    DWORD                       dwFlags,
  _Inout_ void                        **ppvStoreProvFindInfo,
  _Out_   PCCRL_CONTEXT               *ppProvCrlContext
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

Um ponteiro para uma [**loja de certificados \_ \_ Prov \_ encontrar \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) a estrutura de informações contendo todos os parâmetros passados para a função [**CertFindCRLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcrlinstore) .

</dd> <dt>

*pPrevCrlContext* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura de [**\_ contexto de CRL**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) da última CRL encontrada. Na primeira chamada para a função, esse parâmetro deve ser definido como **NULL**. Em chamadas subsequentes, ele deve ser definido como o ponteiro retornado no parâmetro *ppProvCRLContext* na última chamada. Um ponteiro não **nulo** passado nesse parâmetro é liberado pela função de retorno de chamada.

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Quaisquer valores de sinalizador necessários.

</dd> <dt>

*ppvStoreProvFindInfo* \[ entrada, saída\]
</dt> <dd>

Um ponteiro para um ponteiro para um buffer para retornar as informações do provedor de repositório. Opcionalmente, o retorno de chamada pode retornar um ponteiro para informações de localização internas nesse parâmetro. Após a primeira chamada, esse parâmetro é definido como o ponteiro retornado pela chamada anterior para a função.

</dd> <dt>

*ppProvCrlContext* \[ fora\]
</dt> <dd>

Em uma localização bem-sucedida, um ponteiro para a CRL encontrada é retornado nesse parâmetro.

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

[**informações de localização do repositório de certificados \_ \_ Prov \_ \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info)
</dt> <dt>

[**CertFindCRLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcrlinstore)
</dt> <dt>

[**contexto de CRL \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context)
</dt> </dl>

 

 
