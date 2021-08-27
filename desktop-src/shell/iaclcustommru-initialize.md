---
description: Carrega uma lista de cadeias de caracteres na lista de MRU (usados mais recentemente) do Registro.
title: Método IACLCustomMRU::Initialize
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IACLCustomMRU.Initialize
api_type:
- COM
api_location: ''
ms.assetid: 358921b0-46c4-4428-b0b5-57a44fc3247b
ms.openlocfilehash: 0e0cad5f144a4ce97c648463cfdf31bf1c2ee7da0fb89b5508ce9386dba0f14f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111756"
---
# <a name="iaclcustommruinitialize-method"></a>Método IACLCustomMRU::Initialize

Carrega uma lista de cadeias de caracteres na lista de MRU (usados mais recentemente) do Registro.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Initialize(
  [in] LPCWSTR pwszMRURegKey,
  [in] DWORD   dwMax
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pwszMRURegKey* \[ Em\]
</dt> <dd>

Tipo: **LPCWSTR**

Um ponteiro para um buffer que contém a chave do Registro que contém as cadeias de caracteres da lista mru.

</dd> <dt>

*dwMax* \[ Em\]
</dt> <dd>

Tipo: **DWORD**

O número máximo de entradas que podem ser retiradas de *pwszMRURegKey*.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/> |



 

 




