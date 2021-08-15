---
description: Enumera ou localiza a primeira ou a próxima CTL em um repositório externo que corresponde aos critérios especificados.
ms.assetid: 0b465e6e-fb5c-4621-a968-c2cdcab0ea15
title: Função de retorno de chamada CertStoreProvFindCTL
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFindCTL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: f3064b42961196a7522fba6d08ac684aa4421b26727cdf229854351c777a4b56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117769993"
---
# <a name="certstoreprovfindctl-callback-function"></a>Função de retorno de chamada CertStoreProvFindCTL

A função de retorno de chamada **CertStoreProvFindCTL** enumera ou localiza a primeira ou a próxima [*CTL*](../secgloss/c-gly.md) em um [*repositório externo*](../secgloss/e-gly.md) que corresponde aos critérios especificados.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI CertStoreProvFindCTL(
  _In_    HCERTSTOREPROV              hStoreProv,
  _In_    PCCERT_STORE_PROV_FIND_INFO pFindInfo,
  _In_    PCCTL_CONTEXT               pPrevCtlContext,
  _In_    DWORD                       dwFlags,
  _Inout_ void                        **ppvStoreProvFindInfo,
  _Out_   PCCTL_CONTEXT               *ppProvCtlContext
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

Um ponteiro para uma [**loja de certificados \_ \_ Prov \_ encontrar \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) a estrutura de informações contendo todos os parâmetros passados para o [**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore). .

</dd> <dt>

*pPrevCtlContext* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura de [**\_ contexto de CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) da última CTL encontrada. Na primeira chamada para a função, esse parâmetro deve ser definido como **NULL**. Em chamadas subsequentes, ele deve ser definido como o ponteiro retornado no parâmetro *ppProvCTLContext* na última chamada. Um ponteiro não **nulo** passado nesse parâmetro é liberado pela função de retorno de chamada.

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Quaisquer valores de sinalizador necessários.

</dd> <dt>

*ppvStoreProvFindInfo* \[ entrada, saída\]
</dt> <dd>

Um ponteiro para um ponteiro para o buffer para retornar as informações do provedor de repositório. Opcionalmente, o retorno de chamada pode retornar um ponteiro para informações de localização internas nesse parâmetro. Após a primeira chamada, esse parâmetro é definido como o ponteiro retornado pela chamada anterior para a função.

</dd> <dt>

*ppProvCtlContext* \[ fora\]
</dt> <dd>

Em uma localização bem-sucedida, um ponteiro para a CTL encontrada é retornado nesse parâmetro.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **true** se a função for bem-sucedida ou **false** se falhar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>          |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**informações de localização do repositório de certificados \_ \_ Prov \_ \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info)
</dt> <dt>

[**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore)
</dt> <dt>

[**contexto de CTL \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context)
</dt> </dl>

 

 
