---
description: A interface IAMTimeline fornece métodos para manipular a linha do tempo, o objeto central no Microsoft DirectShow Editing Services (DES).
ms.assetid: 6750efa0-946c-4ad3-b0df-de55872b94c3
title: Interface IAMTimeline (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fc4374a198232625b87448004b667ccd8ce0183b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758685"
---
# <a name="iamtimeline-interface"></a>Interface IAMTimeline

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

A `IAMTimeline` interface fornece métodos para manipular a linha do tempo, o objeto central no [Microsoft DirectShow Editing Services](directshow-editing-services.md) (des). Uma linha do tempo é uma coleção de elementos ordenados por tempo, como clipes de vídeo, clipes de áudio, efeitos e transições entre clipes. O mecanismo de renderização usa a linha do tempo para criar um gráfico de filtro, a partir do qual o aplicativo pode gerar a saída renderizada.

`IAMTimeline` executa três serviços básicos. Ele

-   Cria os objetos na linha do tempo.
-   Atua como um contêiner para esses objetos.
-   Define e recupera parâmetros gerais da linha do tempo.

Para criar o objeto Timeline, chame **CoCreateInstance** com o identificador de classe CLSID \_ AMTimeline.

## <a name="members"></a>Membros

A interface **IAMTimeline** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IAMTimeline** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IAMTimeline** tem esses métodos.



| Método                                                             | Descrição                                                                                                                       |
|:-------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [**AddGroup**](iamtimeline-addgroup.md)                           | Adiciona um grupo à linha do tempo.<br/>                                                                                          |
| [**ClearAllGroups**](iamtimeline-clearallgroups.md)               | Remove todos os grupos da linha do tempo, juntamente com todos os objetos contidos nesses grupos.<br/>                                |
| [**CreateEmptyNode**](iamtimeline-createemptynode.md)             | Cria um novo objeto de linha do tempo.<br/>                                                                                         |
| [**EffectsEnabled**](iamtimeline-effectsenabled.md)               | Determina se os efeitos estão habilitados.<br/>                                                                                |
| [**EnableEffects**](iamtimeline-enableeffects.md)                 | Habilita ou desabilita todos os efeitos na linha do tempo.<br/>                                                                       |
| [**EnableTransitions**](iamtimeline-enabletransitions.md)         | Habilita ou desabilita todas as transições na linha do tempo.<br/>                                                                   |
| [**GetCountOfType**](iamtimeline-getcountoftype.md)               | Recupera o número de objetos do tipo especificado que estão contidos em um grupo especificado e todos os seus filhos.<br/> |
| [**GetDefaultEffect**](iamtimeline-getdefaulteffect.md)           | Recupera o efeito padrão.<br/>                                                                                          |
| [**GetDefaultEffectB**](iamtimeline-getdefaulteffectb.md)         | Recupera o efeito padrão como um valor **BSTR** .<br/>                                                                      |
| [**GetDefaultFPS**](iamtimeline-getdefaultfps.md)                 | Recupera a taxa de quadros de saída padrão, em quadros por segundo.<br/>                                                         |
| [**GetDefaultTransition**](iamtimeline-getdefaulttransition.md)   | Recupera a transição padrão.<br/>                                                                                      |
| [**GetDefaultTransitionB**](iamtimeline-getdefaulttransitionb.md) | Recupera a transição padrão como um valor de **BSTR** .<br/>                                                                  |
| [**GetDirtyRange**](iamtimeline-getdirtyrange.md)                 | Não há suporte.<br/>                                                                                                         |
| [**GetDuration**](iamtimeline-getduration.md)                     | Recupera a duração da linha do tempo.<br/>                                                                                       |
| [**GetDuration2**](iamtimeline-getduration2.md)                   | Recupera a duração da linha do tempo como um **duplo**.<br/>                                                                       |
| [**Getgroup**](iamtimeline-getgroup.md)                           | Recupera um grupo especificado.<br/>                                                                                           |
| [**GetGroupCount**](iamtimeline-getgroupcount.md)                 | Recupera o número de grupos contidos na linha do tempo.<br/>                                                     |
| [**Getinsertmode**](iamtimeline-getinsertmode.md)                 | Não há suporte.<br/>                                                                                                         |
| [**IsDirty**](iamtimeline-isdirty.md)                             | Não há suporte.<br/>                                                                                                         |
| [**RemGroupFromList**](iamtimeline-remgroupfromlist.md)           | Não há suporte.<br/>                                                                                                         |
| [**SetDefaultEffect**](iamtimeline-setdefaulteffect.md)           | Define o efeito padrão.<br/>                                                                                               |
| [**SetDefaultEffectB**](iamtimeline-setdefaulteffectb.md)         | Define o efeito padrão como um valor **BSTR** .<br/>                                                                           |
| [**SetDefaultFPS**](iamtimeline-setdefaultfps.md)                 | Define a taxa de quadros de saída padrão, em quadros por segundo.<br/>                                                              |
| [**SetDefaultTransition**](iamtimeline-setdefaulttransition.md)   | Define a transição padrão.<br/>                                                                                           |
| [**SetDefaultTransitionB**](iamtimeline-setdefaulttransitionb.md) | Define a transição padrão como um valor de BSTR.<br/>                                                                           |
| [**Setinsertmode**](iamtimeline-setinsertmode.md)                 | Não implementado.<br/>                                                                                                       |
| [**SetInterestRange**](iamtimeline-setinterestrange.md)           | Não implementado.<br/>                                                                                                       |
| [**TransitionsEnabled**](iamtimeline-transitionsenabled.md)       | Determina se as transições estão habilitadas.<br/>                                                                            |
| [**ValidateSourceNames**](iamtimeline-validatesourcenames.md)     | Valida os nomes de origem na linha do tempo.<br/>                                                                                |



 

## <a name="remarks"></a>Comentários

> [!Note]  
> O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>QEdit. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



 

 
