---
description: Pesquisa a próxima combinação tag dentro do pai especificado e retorna o TAGID da match.
ms.assetid: c96aa1c1-b0e6-49f5-9f74-7d0e050bee3b
title: Função SdbFindNextTag
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFindNextTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: fe9b9914ed9126a364fb377adc4afae84784df156a8e75c3d0d2f997f6185811
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103696"
---
# <a name="sdbfindnexttag-function"></a>Função SdbFindNextTag

Pesquisa a próxima combinação tag dentro do pai especificado e retorna **o TAGID** da match.

## <a name="syntax"></a>Sintaxe


```C++
TAGID WINAPI SdbFindNextTag(
  _In_ PDB   pdb,
  _In_ TAGID tiParent,
  _In_ TAGID tiPrev
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pdb* \[ Em\]
</dt> <dd>

Um alça para o banco de dados shim.

</dd> <dt>

*tiParent* \[ Em\]
</dt> <dd>

O **TAGID** do início da pesquisa. Esse parâmetro pode ser **TAGID \_ ROOT ou** **TAG TYPE \_ \_ LIST.**

</dd> <dt>

*tiPrev* \[ Em\]
</dt> <dd>

O **TAGID** da corresponder anterior.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O **TAGID** da combinação.

## <a name="remarks"></a>Comentários

Antes de chamar essa função, chame a [**função SdbFindFirstTag.**](sdbfindfirsttag.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SdbFindFirstTag**](sdbfindfirsttag.md)
</dt> <dt>

[**SdbTagRefToTagID**](sdbtagreftotagid.md)
</dt> </dl>

 

 




