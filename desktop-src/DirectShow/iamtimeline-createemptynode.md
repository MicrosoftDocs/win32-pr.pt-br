---
description: O método CreateEmptyNode cria um novo objeto Timeline.
ms.assetid: 64184bfd-6f93-4865-81e7-b1ed7b7148aa
title: 'Método IAMTimeline:: CreateEmptyNode (QEdit. h)'
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
ms.openlocfilehash: 894126bea8f40537602aa1fe8898038245215914
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757684"
---
# <a name="iamtimelinecreateemptynode-method"></a>Método IAMTimeline:: CreateEmptyNode

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `CreateEmptyNode` método cria um novo objeto de linha do tempo.

Use esse método para criar objetos de linha do tempo, em vez da função **CoCreateInstance** , porque esse método executa rotinas de inicialização importantes. Cada objeto criado por esse método dá suporte a pelo menos a interface [**IAMTimelineObj**](iamtimelineobj.md) , juntamente com outras interfaces específicas para esse tipo de objeto.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CreateEmptyNode(
  [out] IAMTimelineObj      **ppObj,
        TIMELINE_MAJOR_TYPE Type
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppObj* \[ fora\]
</dt> <dd>

Recebe um ponteiro para a interface [**IAMTimelineObj**](iamtimelineobj.md) do novo objeto.

</dd> <dt>

*Tipo* 
</dt> <dd>

Membro do tipo enumerado de [**\_ \_ tipo principal da linha do tempo**](timeline-major-type.md) , especificando o tipo de objeto a ser criado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Não adicione o novo objeto a outra instância da linha do tempo. Cada objeto em uma linha do tempo deve ser criado por essa linha do tempo.

Se o método for executado com sucesso, a interface [**IAMTimelineObj**](iamtimelineobj.md) que ele retornar terá uma contagem de referência pendente. Certifique-se de liberar a interface quando terminar de usá-la.

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

[**Interface IAMTimeline**](iamtimeline.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




