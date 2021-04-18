---
description: O método ConnectFrontEnd cria o front-end do grafo de filtro a partir da linha do tempo atual.
ms.assetid: ac484fd6-b88d-4c3a-bc4d-f118083d706d
title: 'Método IRenderEngine:: ConnectFrontEnd (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.ConnectFrontEnd
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 58ebd8e162f376b6ef942397e601139c46d8e4cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778433"
---
# <a name="irenderengineconnectfrontend-method"></a>Método IRenderEngine:: ConnectFrontEnd

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `ConnectFrontEnd` método cria o front-end do grafo de filtro a partir da linha do tempo atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ConnectFrontEnd();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os possíveis valores de retorno incluem o seguinte:



| Código de retorno                                                                                                  | Descrição                                                                    |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                         | Êxito.<br/>                                                            |
| <dl> <dt>**S \_ avisar \_ OUTPUTRESET**</dt> </dl>          | A parte de renderização do grafo foi excluída.<br/>                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                 | Nenhuma linha do tempo definida para este mecanismo de renderização.<br/>                             |
| <dl> <dt>**E \_ deve \_ iniciar o \_ renderizador**</dt> </dl>       | Falha ao inicializar o mecanismo de renderização.<br/>                                 |
| <dl> <dt>**o \_ mecanismo de renderização E \_ \_ está \_ desfeito**</dt> </dl> | Falha na operação porque o projeto não foi renderizado com êxito.<br/> |
| <dl> <dt>**E \_ inesperado**</dt> </dl>                 | Erro inesperado.<br/>                                                   |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl>      | Tipo de mídia inválido.<br/>                                                 |



 

## <a name="remarks"></a>Comentários

Esse método não cria a parte de renderização do grafo de filtro. O aplicativo deve conectar os Pins de saída no front-end para os filtros de renderização desejados:

-   Para visualizar, chame o método [**IRenderEngine:: RenderOutputPins**](irenderengine-renderoutputpins.md) .
-   Para gerar um arquivo, chame [**IRenderEngine:: GetGroupOutputPin**](irenderengine-getgroupoutputpin.md) para recuperar o pino de saída para cada grupo e, em seguida, conecte os Pins a um filtro Multiplexador.

Se você estiver usando o mecanismo de processamento básico, os Pins de saída no front-end produzirão dados descompactados. Se você estiver usando o mecanismo de processamento inteligente, os Pins de saída produzirão dados compactados.

Se você alterar a linha do tempo depois de criar o gráfico de filtro, deverá chamar `ConnectFrontEnd` novamente para recriar o front-end. O método preserva a parte de renderização do grafo sempre que possível. No entanto, se você adicionar ou excluir um grupo, ou alterar a ordem dos grupos, `ConnectFrontEnd` o excluirá a parte de renderização e seu aplicativo deverá reconstruí-la. Se o método excluir a parte de renderização, ele retornará S \_ Warn \_ OUTPUTRESET.

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

 

 




