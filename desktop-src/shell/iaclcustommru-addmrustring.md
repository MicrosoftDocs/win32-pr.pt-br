---
description: Adiciona uma entrada à lista de MRU (usados mais recentemente).
title: Método IACLCustomMRU::AddMRUString
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IACLCustomMRU.AddMRUString
api_type:
- COM
api_location: ''
ms.assetid: d8fb8fa5-452b-45fd-b015-d9bf3d0c642e
ms.openlocfilehash: 300474dde82274c668e52d9fe9910634d0ac904c
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841997"
---
# <a name="iaclcustommruaddmrustring-method"></a>Método IACLCustomMRU::AddMRUString

Adiciona uma entrada à lista de MRU (usados mais recentemente).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AddMRUString(
  [in] LPCWSTR pwszEntry
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pwszEntry* \[ Em\]
</dt> <dd>

Tipo: **LPCWSTR**

Um ponteiro para um buffer que contém a nova entrada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente \[ aplicativos da área de trabalho do Windows XP\]<br/>          |
| Servidor mínimo com suporte<br/> | Somente aplicativos da área de trabalho do Windows Server 2003 \[\]<br/> |



 

 




