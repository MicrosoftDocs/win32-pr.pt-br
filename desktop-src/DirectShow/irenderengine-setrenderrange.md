---
description: O método SetRenderRange define o intervalo de tempo na linha do tempo a ser renderizado. Os objetos que ficam fora do intervalo especificado não são renderizados e os recursos não são alocados para eles.
ms.assetid: 2dcdca6b-2bae-4a27-bfbc-19a9b2ea633a
title: 'Método IRenderEngine:: SetRenderRange (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetRenderRange
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0255b7806e2e2303bb2ca953fc5e59886480cbf3525d4de1bf1ef2fbd1388caf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952515"
---
# <a name="irenderenginesetrenderrange-method"></a>Método IRenderEngine:: SetRenderRange

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `SetRenderRange` método define o intervalo de tempo na linha do tempo a ser renderizado. Os objetos que ficam fora do intervalo especificado não são renderizados e os recursos não são alocados para eles.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetRenderRange(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Iniciar* 
</dt> <dd>

Hora de início, em unidades de 100 a nanossegundos.

</dd> <dt>

*Parar* 
</dt> <dd>

Hora de parada, em unidades de 100 a nanossegundos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos seguintes valores de **HRESULT** :



| Código de retorno                                                                                            | Descrição                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Êxito.<br/>                            |
| <dl> <dt>**E \_ deve \_ iniciar o \_ renderizador**</dt> </dl> | Falha ao inicializar o mecanismo de renderização.<br/> |



 

## <a name="remarks"></a>Comentários

> [!Note]  
> O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.

 

> [!Note]  
> para obter o Qedit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.

 

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

 

 




