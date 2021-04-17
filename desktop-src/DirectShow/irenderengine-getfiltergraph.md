---
description: O método GetFilterGraph recupera o grafo de filtro que o mecanismo de processamento construiu, se houver.
ms.assetid: 509b2c9c-c21b-4855-880f-f09ad342e758
title: 'Método IRenderEngine:: GetFilterGraph (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.GetFilterGraph
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4c4750e6127c0d57758e46b2309f4d91afc110e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780633"
---
# <a name="irenderenginegetfiltergraph-method"></a>Método IRenderEngine:: GetFilterGraph

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `GetFilterGraph` método recupera o gráfico de filtro que o mecanismo de processamento construiu, se houver.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetFilterGraph(
  [out] IGraphBuilder **ppFG
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppFG* \[ fora\]
</dt> <dd>

Recebe um ponteiro para a interface [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) do grafo de filtro. Ele receberá o valor **NULL** se não houver nenhum grafo de filtro.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos seguintes valores de **HRESULT** :



| Código de retorno                                                                                            | Descrição                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Êxito.<br/>                            |
| <dl> <dt>**E \_ deve \_ iniciar o \_ renderizador**</dt> </dl> | Falha ao inicializar o mecanismo de renderização.<br/> |
| <dl> <dt>**\_ponteiro E**</dt> </dl>              | Ponteiro inválido.<br/>                    |



 

## <a name="remarks"></a>Comentários

Use o método [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md) para criar o front-end do grafo de filtro. Para a versão prévia, use [**IRenderEngine:: RenderOutputPins**](irenderengine-renderoutputpins.md) para concluir o grafo. Para saída de arquivo, conecte o front-end a uma combinação de gravador de MUX/arquivo. Para obter mais informações, consulte [renderizando um projeto](rendering-a-project.md).

O grafo resultante pode ser executado, pausado, parado e buscado; no entanto, a taxa de reprodução não pode ser alterada.

No retorno, se o valor de *\* ppFG* for não **nulo**, a interface **IGraphBuilder** terá uma contagem de referência pendente. Certifique-se de liberar a interface quando terminar de usá-la.

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

 

 




