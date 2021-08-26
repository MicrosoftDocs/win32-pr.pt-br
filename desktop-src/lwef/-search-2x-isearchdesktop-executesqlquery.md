---
title: Método ExecuteSQLQuery ISearchDesktop
description: Leva um ponteiro para uma cadeia de caracteres que contém uma consulta linguagem SQL (SQL) e seus atributos e retorna um ponteiro para o conjunto de retorno.
ms.assetid: df3f473b-0bee-4035-abf8-dbe5249ef0ed
keywords:
- Método ExecuteSQLQuery herdado Windows de ambiente
- Método ExecuteSQLQuery herdado Windows recursos de ambiente, interface ISearchDesktop
- Interface ISearchDesktop Herdada Windows recursos de ambiente, método ExecuteSQLQuery
topic_type:
- apiref
api_name:
- ISearchDesktop.ExecuteSQLQuery
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ec436a427958988e7605673b12b3fd8dc6fd3e1a54ab61cc5f542f0494c34923
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014286"
---
# <a name="isearchdesktopexecutesqlquery-method"></a>Método ISearchDesktop::ExecuteSQLQuery

> [!NOTE]
> Windows A Pesquisa de Área de Trabalho 2.x é uma tecnologia obsoleta que estava originalmente disponível como um complemento para Windows XP e Windows Server 2003. Em versões posteriores, use a [API Windows Search.](../search/-search-reference-entry-page.md) 

Leva um ponteiro para uma cadeia de caracteres que contém uma consulta linguagem SQL (SQL) e seus atributos e retorna um ponteiro para o conjunto de retorno.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ExecuteSQLQuery(
  [in]  LPCWSTR *pdwAttributes,
  [in]  LPCWSTR pwszURL,
  [out] ppidUrl *ppidUrl
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pdwAttributes* \[ Em\]
</dt> <dd>

Tipo: **LPCWSTR \***

Uma cadeia de caracteres que contém os outros atributos da consulta.

</dd> <dt>

*pwszURL* \[ Em\]
</dt> <dd>

Tipo: **LPCWSTR**

Uma cadeia de caracteres que contém SQL consulta.

</dd> <dt>

*ppidUrl* \[ out\]
</dt> <dd>

Tipo: **ppidUrl \***

Quando esse método retorna com êxito, contém um ponteiro para o registro retornado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

 

 




