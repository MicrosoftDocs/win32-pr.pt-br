---
description: O método GetFilterGraph recupera o grafo de filtro construído pelo mecanismo de renderização, se for o caso.
ms.assetid: 509b2c9c-c21b-4855-880f-f09ad342e758
title: Método IRenderEngine::GetFilterGraph (Qedit.h)
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
ms.openlocfilehash: 8208d886cd23dab797a9f89d3c050c9f46eff60c8cdd78c27c89dae7396c557a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118397577"
---
# <a name="irenderenginegetfiltergraph-method"></a>Método IRenderEngine::GetFilterGraph

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O método recupera o grafo de filtro construído pelo mecanismo de `GetFilterGraph` renderização, se for o caso.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetFilterGraph(
  [out] IGraphBuilder **ppFG
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppFG* \[ out\]
</dt> <dd>

Recebe um ponteiro para a interface [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) do grafo de filtro. Ele receberá o valor **NULL se** não houver nenhum grafo de filtro.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos seguintes **valores HRESULT:**



| Código de retorno                                                                                            | Descrição                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Êxito.<br/>                            |
| <dl> <dt>**E \_ DEVE \_ INIT \_ RENDERER**</dt> </dl> | Falha na inicialização do mecanismo de renderização.<br/> |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>              | Ponteiro inválido.<br/>                    |



 

## <a name="remarks"></a>Comentários

Use o [**método IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) para criar o front-end do grafo de filtro. Para versão prévia, use [**IRenderEngine::RenderOutputPins**](irenderengine-renderoutputpins.md) para concluir o grafo. Para saída de arquivo, conecte o front-end a uma combinação mux/file writer. Para obter mais informações, consulte [Renderizar um Project](rendering-a-project.md).

O grafo resultante pode ser executado, pausado, interrompido e buscado; no entanto, a taxa de reprodução não pode ser alterada.

No retorno, se o valor de *\* ppFG* for não **NULL,** a interface **IGraphBuilder** terá uma contagem de referência pendente. Certifique-se de liberar a interface quando terminar de usá-la.

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

[**IRenderEngine Interface**](irenderengine.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




