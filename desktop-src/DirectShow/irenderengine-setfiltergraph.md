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
ms.openlocfilehash: 4472d1152d45ee160885a4cdbc898a55ece24b6795a9880a5eeb958e05330287
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767096"
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

## <a name="return-value"></a>Valor retornado

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

o método **ConnectFrontEnd** destrói qualquer grafo de filtro existente, mas mantém o mesmo filtro Graph instância do gerenciador.

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

 

 




