---
description: O método CreateEmptyNode cria um novo objeto de linha do tempo.
ms.assetid: 64184bfd-6f93-4865-81e7-b1ed7b7148aa
title: Método IAMTimeline::CreateEmptyNode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.CreateEmptyNode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0f98073c7e3a4be7fa57858440e540769eef50c44fae4ddcaed459146bfc788a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119389136"
---
# <a name="iamtimelinecreateemptynode-method"></a>Método IAMTimeline::CreateEmptyNode

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `CreateEmptyNode` método cria um novo objeto de linha do tempo.

Use esse método para criar objetos de linha do tempo, em vez da **função CoCreateInstance,** porque esse método executa rotinas de inicialização importantes. Cada objeto criado por esse método dá suporte a pelo menos a interface [**IAMTimelineObj,**](iamtimelineobj.md) juntamente com outras interfaces específicas para esse tipo de objeto.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CreateEmptyNode(
  [out] IAMTimelineObj      **ppObj,
        TIMELINE_MAJOR_TYPE Type
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppObj* \[ out\]
</dt> <dd>

Recebe um ponteiro para a interface [**IAMTimelineObj**](iamtimelineobj.md) do novo objeto.

</dd> <dt>

*Tipo* 
</dt> <dd>

Membro do tipo [**enumerado TIMELINE \_ MAJOR \_ TYPE,**](timeline-major-type.md) especificando o tipo de objeto a ser criado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

Não adicione o novo objeto a outra instância de linha do tempo. Cada objeto em uma linha do tempo deve ser criado por essa linha do tempo.

Se o método for bem-sucedido, a interface [**IAMTimelineObj**](iamtimelineobj.md) retornada terá uma contagem de referência pendente. Certifique-se de liberar a interface quando terminar de usá-la.

> [!Note]  
> O arquivo de título Qedit.h não é compatível com os headers direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o Qedit.h, baixe [o Microsoft Windows SDK Update para Windows Vista e .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O Qedit.h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IAMTimeline Interface**](iamtimeline.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




