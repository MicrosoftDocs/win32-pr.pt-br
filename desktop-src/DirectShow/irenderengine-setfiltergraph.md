---
description: O método SetFilterGraph especifica um grafo de filtro para o mecanismo de renderização usar.
ms.assetid: 6a245864-7d22-4608-995b-b28662a6ab90
title: 'Método IRenderEngine:: SetFilterGraph (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetFilterGraph
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 72c93ef6610fd301c497589858a8941e2b8f71b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789934"
---
# <a name="irenderenginesetfiltergraph-method"></a>Método IRenderEngine:: SetFilterGraph

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `SetFilterGraph` método especifica um grafo de filtro para o mecanismo de renderização usar.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetFilterGraph(
   IGraphBuilder *pFG
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pFG* 
</dt> <dd>

Ponteiro para a interface [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) do grafo de filtro.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos seguintes valores de **HRESULT** :



| Código de retorno                                                                                            | Descrição                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Êxito.<br/>                            |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>           | Argumento inválido.<br/>                   |
| <dl> <dt>**E \_ deve \_ iniciar o \_ renderizador**</dt> </dl> | Falha ao inicializar o mecanismo de renderização.<br/> |



 

## <a name="remarks"></a>Comentários

A maioria dos aplicativos não precisa chamar esse método. É mais comum deixar o mecanismo de renderização criar o grafo para você, chamando o método [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md) .

Esse método falhará se o mecanismo de processamento já tiver um grafo de filtro.

Nunca recupere um ponteiro para um grafo de filtro criado por um mecanismo de renderização e, em seguida, use-o como o parâmetro para esse método em outro mecanismo de renderização. Isso causará resultados imprevisíveis.

O método **ConnectFrontEnd** destrói qualquer grafo de filtro existente, mas mantém a mesma instância de Gerenciador de gráfico de filtros.

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

 

 




