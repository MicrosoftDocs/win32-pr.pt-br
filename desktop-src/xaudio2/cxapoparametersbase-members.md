---
description: Mostra os membros da classe CXAPOParametersBase.
ms.assetid: C2113358-07DE-426E-AF26-BD8ED9902192
title: Membros do CXAPOParametersBase
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e225d1628408b5d5472bed8c3060f714bb7b0ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105765002"
---
# <a name="cxapoparametersbase-members"></a>Membros do CXAPOParametersBase

Mostra os membros da classe [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) .

## <a name="public-constructors"></a>Construtores públicos



|                                                    |                                                                         |
|----------------------------------------------------|-------------------------------------------------------------------------|
| [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) | Constrói um objeto [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) . |



 

## <a name="public-methods"></a>Métodos públicos



|                                                                                                                              |                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddRef**](/previous-versions/windows/desktop/legacy/ee418448(v=vs.85)) (Herdado de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                                         | Incrementa a contagem de referência do objeto XAPO.<br/>                                                                                                         |
| [**BeginProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess)                                                                     | Retorna os parâmetros do processo atual. <br/>                                                                                                              |
| [**CalcInputFrames**](/windows/win32/api/xapo/nf-xapo-ixapo-calcinputframes) (Herdado de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                           | Retorna o número de quadros de entrada necessários para gerar o número determinado de quadros de saída.<br/>                                                            |
| [**CalcOutputFrames**](/windows/win32/api/xapo/nf-xapo-ixapo-calcoutputframes) (Herdado de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                         | Retorna o número de quadros de saída necessários para gerar o número determinado de quadros de entrada.<br/>                                                            |
| [**Fim do processo**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-endprocess)                                                                         | Notifica [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) que o XAPO terminou de acessar os parâmetros do processo atual. <br/>                     |
| [**Parameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-getparameters) (Herdado de [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters)) | Obtém parâmetros específicos de efeito. <br/>                                                                                                                     |
| [**Getregistrationproperties**](/windows/win32/api/xapo/nf-xapo-ixapo-getregistrationproperties) (Herdado de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))       | Retorna as propriedades de registro de um XAPO.<br/>                                                                                                       |
| [**Initialize**](/windows/win32/api/xapo/nf-xapo-ixapo-initialize) (Herdado de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                                     | Executa qualquer inicialização específica de efeito.<br/>                                                                                                          |
| [**IsInputFormatSupported**](/windows/win32/api/xapo/nf-xapo-ixapo-isinputformatsupported) (Herdado de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))             | Consulta se um formato de entrada específico tem suporte para um determinado formato de saída.<br/>                                                                            |
| [**IsOutputFormatSupported**](/windows/win32/api/xapo/nf-xapo-ixapo-isoutputformatsupported) (Herdado de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))           | Consulta se um formato de saída específico tem suporte para um determinado formato de entrada.<br/>                                                                            |
| [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) (Herdado de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                             | Notifica XAPO de que o [**processo**](/windows/win32/api/xapo/nf-xapo-ixapo-process) de formatos de fluxo será fornecido.<br/>                                                             |
| [**OnSetParameters**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-onsetparameters)                                                               | Chamado por [**IXAPOParameters:: Parameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) para permitir a validação de parâmetro definida pelo usuário. <br/>          |
| [**Parâmetroschanged**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-parameterschanged)                                                           | Indica se [**IXAPOParameters:: Parameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) foi chamado desde a última passagem de processamento. <br/>       |
| [**QueryInterface**](/previous-versions/windows/desktop/legacy/ee418457(v=vs.85)) (Herdado de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                         | Recupera o ponteiro de interface solicitado se o XAPO der suporte a ele.<br/>                                                                                    |
| [**Versão**](/previous-versions/windows/desktop/legacy/ee418458(v=vs.85)) (herdada de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                                       | Decrementa a contagem de referência do objeto XAPO e exclui o objeto se a contagem de referência cair em zero.<br/>                                             |
| [**Redefinir**](/windows/win32/api/xapo/nf-xapo-ixapo-reset) (Herdado de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                                               | Retorna o objeto para o estado em que ele estava logo após a chamada de [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) .<br/>                             |
| [**Parameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) (Herdado de [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters)) | Define parâmetros específicos de efeito.<br/>                                                                                                                      |
| [**UnlockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-unlockforprocess) (Herdado de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                         | Oposto de LockForProcess: as variáveis alocadas durante [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) devem ser desalocadas nesse método.<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Classe CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase)
</dt> </dl>

 

 
