---
description: Pesquisa o executável especificado.
ms.assetid: 32c6b054-7e47-4427-bdfe-6b5066db4ac3
title: Função SdbGetMatchingExe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetMatchingExe
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 9d9c8c8c5e9ba0c55068558698b40c7274929364
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826355"
---
# <a name="sdbgetmatchingexe-function"></a>Função SdbGetMatchingExe

Pesquisa o executável especificado.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI SdbGetMatchingExe(
  _In_opt_ HSDB            hSDB,
  _In_     LPCTSTR         szPath,
  _In_opt_ LPCTSTR         szModuleName,
  _In_opt_ LPCTSTR         pszEnvironment,
  _In_     DWORD           dwFlags,
  _Out_    PSDBQUERYRESULT pQueryResult
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hSDB* \[ em, opcional\]
</dt> <dd>

Um identificador para o banco de dados de Shim retornado pela função [**SdbInitDatabase**](sdbinitdatabase.md) .

</dd> <dt>

*szPath* \[ no\]
</dt> <dd>

O caminho do executável.

</dd> <dt>

*szModuleName* \[ em, opcional\]
</dt> <dd>

O nome do módulo.

</dd> <dt>

*pszEnvironment* \[ em, opcional\]
</dt> <dd>

As variáveis de ambiente a serem usadas como contexto de pesquisa.

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Esse parâmetro pode ser 0 ou **SDBGMEF \_ ignorar \_ ambiente** (0x1).

</dd> <dt>

*pQueryResult* \[ fora\]
</dt> <dd>

Uma estrutura [**SDBQUERYRESULT**](sdbqueryresult.md) . Se nenhuma correspondência for encontrada, a estrutura conterá **TAGREF \_ nulo**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

A função retorna **true** em caso de êxito ou **false** em caso de falha.

## <a name="remarks"></a>Comentários

Quando você terminar com o [**TAGREF**](tagref.md)retornado, libere-o usando a função [**SdbReleaseMatchingExe**](sdbreleasematchingexe.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SdbInitDatabase**](sdbinitdatabase.md)
</dt> <dt>

[**SdbReleaseMatchingExe**](sdbreleasematchingexe.md)
</dt> </dl>

 

 




