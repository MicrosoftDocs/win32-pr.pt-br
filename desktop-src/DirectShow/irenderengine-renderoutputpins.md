---
description: O método RenderOutputPins cria a parte de visualização do grafo de filtro.
ms.assetid: 66bcb698-cd85-4c22-bfef-2e51973958f1
title: Método IRenderEngine::RenderOutputPins (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.RenderOutputPins
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b81ea650d805c8ed2e42797f4dffdd9851eb3f072cff0abb05f54c4581684bea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818558"
---
# <a name="irenderenginerenderoutputpins-method"></a>Método IRenderEngine::RenderOutputPins

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `RenderOutputPins` método cria a parte de visualização do grafo de filtro.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT RenderOutputPins();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna valores **HRESULT.** O valores possíveis são os seguintes:



| Código de retorno                                                                                                  | Descrição                                                                |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                         | Êxito.<br/>                                                        |
| <dl> <dt>**ÁUDIO DO VFW \_ NÃO \_ \_ \_ RENDERIZADO**</dt> </dl>  | Não é possível reproduzir o fluxo de áudio.<br/>                              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                 | Argumento inválido.<br/>                                               |
| <dl> <dt>**O \_ MECANISMO \_ DE RENDERIZAÇÃO E ESTÁ \_ \_ DESFEITO**</dt> </dl> | Falha na operação porque o projeto não foi renderizado com êxito.<br/> |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl>                 | Erro inesperado.<br/>                                               |



 

## <a name="remarks"></a>Comentários

Antes de chamar esse método, chame [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) para criar o front-end do grafo. Para executar uma operação diferente da versão prévia, não chame esse método. Em vez disso, [**chame IRenderEngine::GetGroupOutputPin**](irenderengine-getgroupoutputpin.md) para obter ponteiros para os pinos de saída.

Se não houver nenhuma placa de som no computador do usuário, esse método retornará O ÁUDIO \_ NÃO \_ RENDERIZADO do VFW. \_ \_ Não haverá visualização de áudio nesse caso, mas a visualização de vídeo não será afetada.

Se o pin for de um grupo de vídeo, esse método criará uma janela de vídeo. O thread de chamada deve expedir mensagens – por exemplo, para mover a janela ou responder a cliques do mouse na área do cliente da janela.

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

 

 




