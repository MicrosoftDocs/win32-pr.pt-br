---
description: Carrega uma lista de cadeias de caracteres na lista MRU (usada mais recentemente) do registro.
title: 'Método IACLCustomMRU:: Initialize'
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
ms.openlocfilehash: 715c6991021070dd132942de0bb18c8b77684860
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841227"
---
# <a name="iaclcustommruinitialize-method"></a>Método IACLCustomMRU:: Initialize

Carrega uma lista de cadeias de caracteres na lista MRU (usada mais recentemente) do registro.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Initialize(
  [in] LPCWSTR pwszMRURegKey,
  [in] DWORD   dwMax
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pwszMRURegKey* \[ no\]
</dt> <dd>

Tipo: **LPCWSTR**

Um ponteiro para um buffer contendo a chave do registro que contém as cadeias de caracteres da lista MRU.

</dd> <dt>

*dwMax* \[ no\]
</dt> <dd>

Tipo: **DWORD**

O número máximo de entradas que podem ser obtidas de *pwszMRURegKey*.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/> |



 

 




