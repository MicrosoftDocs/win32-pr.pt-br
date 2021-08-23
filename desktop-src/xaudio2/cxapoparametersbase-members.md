---
description: Mostra os membros da classe CXAPOParametersBase.
ms.assetid: C2113358-07DE-426E-AF26-BD8ED9902192
title: Membros CXAPOParametersBase
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ededac8054229cffa7799ced71653ab19cacf74f705e77163556cc5b60b7655d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770835"
---
# <a name="cxapoparametersbase-members"></a>Membros CXAPOParametersBase

Mostra os membros da [**classe CXAPOParametersBase.**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase)

## <a name="public-constructors"></a>Construtores públicos



|    Construtor                                                |     Descrição                                                                    |
|----------------------------------------------------|-------------------------------------------------------------------------|
| [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) | Constrói [**um objeto CXAPOParametersBase.**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) |



 

## <a name="public-methods"></a>Métodos públicos



|        Método                                                                                                                      |     Descrição                                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddRef**](/previous-versions/windows/desktop/legacy/ee418448(v=vs.85)) (herdado de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                                         | Incrementa a contagem de referência do objeto XAPO.<br/>                                                                                                         |
| [**BeginProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess)                                                                     | Retorna os parâmetros de processo atuais. <br/>                                                                                                              |
| [**CalcInputFrames**](/windows/win32/api/xapo/nf-xapo-ixapo-calcinputframes) (herdado de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                           | Retorna o número de quadros de entrada necessários para gerar o número determinado de quadros de saída.<br/>                                                            |
| [**CalcOutputFrames**](/windows/win32/api/xapo/nf-xapo-ixapo-calcoutputframes) (herdado de [**IXAPO)**](/windows/desktop/api/XAPO/nn-xapo-ixapo)                         | Retorna o número de quadros de saída necessários para gerar o número determinado de quadros de entrada.<br/>                                                            |
| [**EndProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-endprocess)                                                                         | Notifica [**CXAPOParametersBase de**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) que o XAPO concluiu o acesso aos parâmetros de processo atuais. <br/>                     |
| [**GetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-getparameters) (herdado de [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters)) | Obtém parâmetros específicos do efeito. <br/>                                                                                                                     |
| [**GetRegistrationProperties**](/windows/win32/api/xapo/nf-xapo-ixapo-getregistrationproperties) (herdado de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))       | Retorna as propriedades de registro de um XAPO.<br/>                                                                                                       |
| [**Inicializar**](/windows/win32/api/xapo/nf-xapo-ixapo-initialize) (herdado de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                                     | Executa qualquer inicialização específica do efeito.<br/>                                                                                                          |
| [**IsInputFormatSupported**](/windows/win32/api/xapo/nf-xapo-ixapo-isinputformatsupported) (herdado de [**IXAPO)**](/windows/desktop/api/XAPO/nn-xapo-ixapo)             | Consulta se há suporte para um formato de entrada específico para um determinado formato de saída.<br/>                                                                            |
| [**IsOutputFormatSupported**](/windows/win32/api/xapo/nf-xapo-ixapo-isoutputformatsupported) (herdado de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))           | Consulta se há suporte para um formato de saída específico para um determinado formato de entrada.<br/>                                                                            |
| [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) (herdado do [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                             | Notifica o XAPO de formatos de fluxo [**O processo**](/windows/win32/api/xapo/nf-xapo-ixapo-process) será determinado.<br/>                                                             |
| [**OnSetParameters**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-onsetparameters)                                                               | Chamado por [**IXAPOParameters::SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) para permitir a validação de parâmetro definida pelo usuário. <br/>          |
| [**Parameterschanged**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-parameterschanged)                                                           | Indica se [**IXAPOParameters::SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) foi chamado desde a última passagem de processamento. <br/>       |
| [**QueryInterface**](/previous-versions/windows/desktop/legacy/ee418457(v=vs.85)) (herdado de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                         | Recupera o ponteiro de interface solicitado se o XAPO dá suporte a ele.<br/>                                                                                    |
| [**Versão**](/previous-versions/windows/desktop/legacy/ee418458(v=vs.85)) (herdada do [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                                       | Diminui a contagem de referência do objeto XAPO e exclui o objeto se a contagem de referência cair para zero.<br/>                                             |
| [**Redefinir**](/windows/win32/api/xapo/nf-xapo-ixapo-reset) (herdado do [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                                               | Retorna o objeto para o estado em que estava logo depois [**que LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) foi chamado.<br/>                             |
| [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) (herdado de [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters)) | Define parâmetros específicos do efeito.<br/>                                                                                                                      |
| [**UnlockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-unlockforprocess) (herdado do [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                         | Oposto de LockForProcess: as variáveis alocadas [**durante LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) devem ser desalocadas nesse método.<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Classe CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase)
</dt> </dl>

 

 
