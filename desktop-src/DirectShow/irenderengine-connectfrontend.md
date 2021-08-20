---
description: O método ConnectFrontEnd cria o front-end do grafo de filtro da linha do tempo atual.
ms.assetid: ac484fd6-b88d-4c3a-bc4d-f118083d706d
title: Método IRenderEngine::ConnectFrontEnd (Qedit.h)
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
ms.openlocfilehash: b7e0b00d467eb56dabaf6623f129ed1eb82945a1add63386b2b21fb01f725082
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118154033"
---
# <a name="irenderengineconnectfrontend-method"></a>Método IRenderEngine::ConnectFrontEnd

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `ConnectFrontEnd` método cria o front-end do grafo de filtro da linha do tempo atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ConnectFrontEnd();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.** Os possíveis valores de retorno incluem o seguinte:



| Código de retorno                                                                                                  | Descrição                                                                    |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                         | Êxito.<br/>                                                            |
| <dl> <dt>**S \_ AVISO \_ OUTPUTRESET**</dt> </dl>          | A parte de renderização do grafo foi excluída.<br/>                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                 | Nenhuma linha do tempo definida para esse mecanismo de renderização.<br/>                             |
| <dl> <dt>**E \_ DEVE \_ INIT \_ RENDERER**</dt> </dl>       | Falha na inicialização do mecanismo de renderização.<br/>                                 |
| <dl> <dt>**O \_ MECANISMO \_ DE RENDERIZAÇÃO E ESTÁ \_ \_ DESFEITO**</dt> </dl> | Falha na operação porque o projeto não foi renderizado com êxito.<br/> |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl>                 | Erro inesperado.<br/>                                                   |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl>      | Tipo de mídia inválido.<br/>                                                 |



 

## <a name="remarks"></a>Comentários

Esse método não cria a parte de renderização do grafo de filtro. O aplicativo deve conectar os pinos de saída no front-end aos filtros de renderização desejados:

-   Para visualizar, chame o [**método IRenderEngine::RenderOutputPins.**](irenderengine-renderoutputpins.md)
-   Para gerar um arquivo, chame [**IRenderEngine::GetGroupOutputPin**](irenderengine-getgroupoutputpin.md) para recuperar o pino de saída para cada grupo e, em seguida, conecte os pinos a um filtro multiplexador.

Se você estiver usando o mecanismo de renderização básico, os pinos de saída no front-end produzirão dados descompactados. Se você estiver usando o mecanismo de renderização inteligente, os pinos de saída produzirão dados compactados.

Se você alterar a linha do tempo depois de criar o grafo de filtro, deverá chamar `ConnectFrontEnd` novamente para recriar o front-end. O método preserva a parte de renderização do grafo sempre que possível. No entanto, se você adicionar ou excluir um grupo ou alterar a ordem dos grupos, excluirá a parte de renderização e seu aplicativo `ConnectFrontEnd` deverá recompagá-lo. Se o método excluir a parte de renderização, ele retornará S \_ WARN \_ OUTPUTRESET.

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

 

 




