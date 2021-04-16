---
description: O método getlocked recupera o estado de edição do objeto (bloqueado ou desbloqueado).
ms.assetid: ecd258db-36bf-41b6-9bdf-537efcf0a46a
title: 'Método IAMTimelineObj:: getlocked (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetLocked
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 472b7dedbdbd879d4fa49fe874fb9178d0ccdee4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779535"
---
# <a name="iamtimelineobjgetlocked-method"></a>Método IAMTimelineObj:: getlocked

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `GetLocked` método recupera o estado de edição do objeto (bloqueado ou desbloqueado). Um estado bloqueado indica que o objeto não deve ser editado; um estado desbloqueado indica que o objeto pode ser editado. A linha do tempo não impõe o bloqueio. A configuração bloqueada existe apenas para a conveniência do aplicativo.

## <a name="syntax"></a>Sintaxe


```C++
 GetLocked(
   BOOL *pVal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pVal* 
</dt> <dd>

Recebe o estado de edição do objeto. Se o valor for **true**, o objeto será bloqueado e não deverá ser editado. Se **for false**, o objeto será desbloqueado e poderá ser editado.

</dd> </dl>

## <a name="remarks"></a>Comentários

> [!Note]  
> O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>QEdit. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IAMTimelineObj**](iamtimelineobj.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




