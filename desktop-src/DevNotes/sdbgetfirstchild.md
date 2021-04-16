---
description: Procura uma marca filho dentro do pai especificado e retorna o TAGID do primeiro filho.
ms.assetid: 67538c7e-6360-40fa-b50f-dcbc7a6a147d
title: Função SdbGetFirstChild
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetFirstChild
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: abc06ae0e4b5d842a968d0f3fbeb7a15702660b9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500738"
---
# <a name="sdbgetfirstchild-function"></a>Função SdbGetFirstChild

Procura uma marca filho dentro do pai especificado e retorna o **TagId** do primeiro filho.

## <a name="syntax"></a>Sintaxe


```C++
TAGID WINAPI SdbGetFirstChild(
  _In_ PDB   pdb,
  _In_ TAGID tiParent
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PDB* \[ no\]
</dt> <dd>

Um identificador para o banco de dados de Shim.

</dd> <dt>

*tiParent* \[ no\]
</dt> <dd>

O **TagId** do início da pesquisa. Esse parâmetro pode ser **TagId \_ raiz** ou **\_ \_ lista de tipos de marca**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O **TagId** do primeiro filho ou **TagId \_ nulo** não é um filho encontrado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SdbFindFirstTag**](sdbfindfirsttag.md)
</dt> <dt>

[**SdbFindNextTag**](sdbfindnexttag.md)
</dt> <dt>

[**SdbGetNextChild**](sdbgetnextchild.md)
</dt> </dl>

 

 




