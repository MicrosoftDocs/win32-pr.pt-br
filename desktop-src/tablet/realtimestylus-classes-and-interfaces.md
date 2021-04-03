---
description: Esta seção contém informações sobre as interfaces e classes usadas na caneta em tempo real.
ms.assetid: fc0900b4-f08b-4a93-bbc0-d3db067d7917
title: Interfaces e classes do RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34769b2c268bcdfe2becf9e759344d972092fe28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828896"
---
# <a name="realtimestylus-classes-and-interfaces"></a>Interfaces e classes do RealTimeStylus

Esta seção contém informações sobre as interfaces e classes usadas na caneta em tempo real.

> [!Note]  
> As classes e interfaces de caneta em tempo real não são compatíveis com a automação.

 

## <a name="in-this-section"></a>Nesta seção



| Classe                                                      | Descrição                                                                                     |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**Classe RealTimeStylus**](realtimestylus-class.md)       | Implementa a interface [**IRealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) .<br/>                 |
| [**Classe DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85))     | Implementa a interface de [**interface IDynamicRenderer**](/windows/desktop/api/RTSCom/nn-rtscom-idynamicrenderer) .<br/>     |
| [**Classe GestureRecognizer**](gesturerecognizer-class.md) | Implementa a interface de [**interface IGestureRecognizer**](/windows/desktop/api/RTSCom/nn-rtscom-igesturerecognizer) .<br/> |
| [**Classe StrokeBuilder**](strokebuilder-class.md)         | Implementa a interface de [**interface IStrokeBuilder**](/windows/desktop/api/RTSCom/nn-rtscom-istrokebuilder) .<br/>         |



 

## <a name="interfaces"></a>Interfaces



| Interface                                                                          | Descrição                                                                                                                                                                                 |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Interface IDynamicRenderer**](/windows/desktop/api/RTSCom/nn-rtscom-idynamicrenderer)                             | Expõe métodos que permitem controlar a exibição de dados da caneta em tempo real à medida que os dados estão sendo manipulados pelo objeto da [**classe RealTimeStylus**](realtimestylus-class.md) .<br/> |
| [**Interface IGestureRecognizer**](/windows/desktop/api/RTSCom/nn-rtscom-igesturerecognizer)                         | Expõe métodos que permitem reagir a eventos reconhecendo gestos da caneta e permitindo que você adicione dados à fila de entrada.<br/>                                                  |
| [**IRealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus)                                         | Manipula os dados de pacote da caneta de um digitalizador em tempo real.<br/>                                                                                                                    |
| [**IRealTimeStylus2**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus2)                                       | Estende a interface IRealTimeStylus.<br/>                                                                                                                                           |
| [**IRealTimeStylus3**](/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus3)                                       | Estende a interface IRealTimeStylus.<br/>                                                                                                                                           |
| [**Interface IRealTimeStylusSynchronization**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylussynchronization) | Sincroniza o acesso ao objeto da [**classe RealTimeStylus**](realtimestylus-class.md) .<br/>                                                                                          |
| [**Interface IStrokeBuilder**](/windows/desktop/api/RTSCom/nn-rtscom-istrokebuilder)                                 | Expõe métodos que permitem criar traços programaticamente.<br/>                                                                                                              |
| [**Interface IStylusPlugin**](/windows/desktop/api/RTSCom/nn-rtscom-istylusplugin)                                   | Expõe métodos que permitem que você receba notificações de eventos e execute o processamento personalizado com base nesses eventos.<br/>                                                          |
| [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin)                                   | Representa um plug-in assíncrono que pode ser adicionado à coleção de plug-ins assíncrono da [**classe RealTimeStylus**](realtimestylus-class.md) .<br/>                                |
| [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin)                                     | Representa um plug-in síncrono que pode ser adicionado à coleção de plug-ins síncrona da [**classe RealTimeStylus**](realtimestylus-class.md) .<br/>                                   |



 

## <a name="return-values"></a>Valores de retorno

Os métodos na biblioteca COM retornam valores de **HRESULT**. Salvo indicação em contrário, os significados dos valores **HRESULT** são descritos na tabela a seguir.



| Valor HRESULT                                   | Description                                                                              |
|-------------------------------------------------|------------------------------------------------------------------------------------------|
| S \_ OK<br/>                                | Êxito.<br/>                                                                      |
| \_ponteiro E<br/>                           | Pelo menos um ponteiro (para um parâmetro de entrada ou de saída) é inválido.<br/> |
| E \_ INVALIDARG<br/>                        | O membro tentou passar um argumento inválido.<br/>                              |
| \_exceção de tinta E \_<br/>                    | Exceção ocorreu.<br/>                                                           |
| E \_ OUTOFMEMORY<br/>                       | O sistema não pode alocar memória para concluir a operação.<br/>                      |
| E \_ falha<br/>                              | Ocorreu uma falha não especificada.<br/>                                                 |
| E \_ INVALIDOPERATION<br/>                  | O membro tentou usar uma operação inválida.<br/>                                 |
| modo do TPC \_ E \_ inválido \_<br/>                | O membro tentou usar um modo inválido.<br/>                                      |
| configuração de TPC \_ E \_ inválido \_<br/>       | O membro tentou usar uma configuração inválida.<br/>                             |
| \_Descrição do pacote TPC E \_ inválido \_ \_<br/> | O membro tentou usar uma descrição de pacote inválida.<br/>                        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência do RealTimeStylus](realtimestylus-reference.md)
</dt> </dl>

 

 
