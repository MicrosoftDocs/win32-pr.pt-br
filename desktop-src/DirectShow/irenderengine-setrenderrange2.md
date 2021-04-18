---
description: 'O método SetRenderRange2 define o intervalo de tempo na linha do tempo a ser renderizado. Esse método é equivalente a IRenderEngine:: SetRenderRange, mas obtém valores do tipo Double.'
ms.assetid: 07df97a8-aa83-405d-91a0-45cd99185588
title: 'Método IRenderEngine:: SetRenderRange2 (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetRenderRange2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 555533b11c96073763af0d2b52823af44e3797be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105786966"
---
# <a name="irenderenginesetrenderrange2-method"></a>Método IRenderEngine:: SetRenderRange2

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `SetRenderRange2` método define o intervalo de tempo na linha do tempo a ser renderizado. Esse método é equivalente a [**IRenderEngine:: SetRenderRange**](irenderengine-setrenderrange.md), mas obtém valores do tipo **Double**.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetRenderRange2(
   double Start,
   double Stop
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Iniciar* 
</dt> <dd>

Hora de início, em segundos.

</dd> <dt>

*Parar* 
</dt> <dd>

Hora de parada, em segundos.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos seguintes valores de **HRESULT** :



| Código de retorno                                                                                            | Descrição                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Êxito.<br/>                            |
| <dl> <dt>**E \_ deve \_ iniciar o \_ renderizador**</dt> </dl> | Falha ao inicializar o mecanismo de renderização.<br/> |



 

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

[**Interface IRenderEngine**](irenderengine.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




