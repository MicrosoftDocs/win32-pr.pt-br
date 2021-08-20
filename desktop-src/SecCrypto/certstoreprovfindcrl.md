---
description: Enumera ou localiza a primeira ou a próxima CRL em um armazenamento externo que corresponde aos critérios especificados.
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
ms.openlocfilehash: eebcc990da0cd2d866325200223e9e654e45e055299a8b384a613dc9841c2799
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126676"
---
# <a name="certstoreprovfindcrl-callback-function"></a>Função de retorno de chamada CertStoreProvFindCRL

A função de retorno de chamada **CertStoreProvFindCRL** enumera ou localiza a primeira ou a próxima [*CRL*](../secgloss/c-gly.md) em um repositório [*externo*](../secgloss/e-gly.md) que corresponde aos critérios especificados.

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

*hStoreProv* \[ Em\]
</dt> <dd>

**Alça HCERTSTOREPROV** para um repositório [*de certificados*](../secgloss/c-gly.md).

</dd> <dt>

*pFindInfo* \[ Em\]
</dt> <dd>

Um ponteiro para uma [**estrutura CERT \_ STORE \_ PROV FIND \_ \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) que contém todos os parâmetros passados para a [**função CertFindCRLInStore.**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcrlinstore)

</dd> <dt>

*pPrevCrlContext* \[ Em\]
</dt> <dd>

Um ponteiro para uma [**estrutura DE CONTEXTO \_ de CRL**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) da última CRL encontrada. Na primeira chamada para a função, esse parâmetro deve ser definido como **NULL.** Em chamadas subsequentes, ele deve ser definido como o ponteiro retornado no *parâmetro ppProvCRLContext* na última chamada. Um ponteiro não **NULL** passado nesse parâmetro é liberado pela função de retorno de chamada.

</dd> <dt>

*dwFlags* \[ Em\]
</dt> <dd>

Quaisquer valores de sinalizador necessários.

</dd> <dt>

*ppvStoreProvFindInfo* \[ in, out\]
</dt> <dd>

Um ponteiro para um ponteiro para um buffer para retornar as informações do provedor de armazenamento. Opcionalmente, o retorno de chamada pode retornar um ponteiro para informações de busca internas neste parâmetro. Após a primeira chamada, esse parâmetro é definido como o ponteiro retornado pela chamada anterior para a função.

</dd> <dt>

*ppProvCrlContext* \[ out\]
</dt> <dd>

Em uma busca bem-sucedida, um ponteiro para a CRL encontrada é retornado nesse parâmetro.

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

[**INFORMAÇÕES \_ DE ENCONTRE O \_ PROV DO ARMAZENAMENTO DE \_ \_ CERTIFICADOS**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info)
</dt> <dt>

[**CertFindCRLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcrlinstore)
</dt> <dt>

[**CONTEXTO \_ DE CRL**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context)
</dt> </dl>

 

 
