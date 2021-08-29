---
description: Mostra os membros da classe CXAPOBase.
ms.assetid: 0791888B-7215-475B-95C8-B558A1E57783
title: Membros do CXAPOBase
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e76e1846b5dd9c28bec4f5cfe8e0168f5afbca012459b5860c4a5e23c610f6ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962735"
---
# <a name="cxapobase-members"></a>Membros do CXAPOBase

Mostra os membros da [**classe CXAPOBase.**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase)

## <a name="public-constructors"></a>Construtores públicos



|                                |                                                     |
|--------------------------------|-----------------------------------------------------|
| [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) | Constrói um [**objeto CXAPOBase.**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) |



 

## <a name="public-methods"></a>Métodos públicos



|                                                                                                                        |                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddRef**](/previous-versions/windows/desktop/legacy/ee418448(v=vs.85)) (herdado de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                                   | Incrementa a contagem de referência do objeto XAPO.<br/>                                                                                                         |
| [**CalcInputFrames**](/windows/win32/api/xapo/nf-xapo-ixapo-calcinputframes) (herdado de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                     | Retorna o número de quadros de entrada necessários para gerar o número determinado de quadros de saída.<br/>                                                            |
| [**CalcOutputFrames**](/windows/win32/api/xapo/nf-xapo-ixapo-calcoutputframes) (herdado de [**IXAPO)**](/windows/desktop/api/XAPO/nn-xapo-ixapo)                   | Retorna o número de quadros de saída necessários para gerar o número determinado de quadros de entrada.<br/>                                                            |
| [**GetRegistrationProperties**](/windows/win32/api/xapo/nf-xapo-ixapo-getregistrationproperties) (herdado de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo)) | Retorna as propriedades de registro de um XAPO.<br/>                                                                                                       |
| [**Inicializar**](/windows/win32/api/xapo/nf-xapo-ixapo-initialize) (herdado de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                               | Executa qualquer inicialização específica do efeito.<br/>                                                                                                          |
| [**IsInputFormatSupported**](/windows/win32/api/xapo/nf-xapo-ixapo-isinputformatsupported) (herdado de [**IXAPO)**](/windows/desktop/api/XAPO/nn-xapo-ixapo)       | Consulta se há suporte para um formato de entrada específico para um determinado formato de saída.<br/>                                                                            |
| [**IsOutputFormatSupported**](/windows/win32/api/xapo/nf-xapo-ixapo-isoutputformatsupported) (herdado de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))     | Consulta se há suporte para um formato de saída específico para um determinado formato de entrada.<br/>                                                                            |
| [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) (herdado do [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                       | Notifica o XAPO de formatos de fluxo [**O processo**](/windows/win32/api/xapo/nf-xapo-ixapo-process) será determinado.<br/>                                                             |
| [**QueryInterface**](/previous-versions/windows/desktop/legacy/ee418457(v=vs.85)) (herdado de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                   | Recupera o ponteiro de interface solicitado se o XAPO dá suporte a ele.<br/>                                                                                    |
| [**Versão**](/previous-versions/windows/desktop/legacy/ee418458(v=vs.85)) (herdada do [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                                 | Decrementa a contagem de referência do objeto XAPO e exclui o objeto se a contagem de referência cair para zero.<br/>                                             |
| [**Redefinir**](/windows/win32/api/xapo/nf-xapo-ixapo-reset) (herdado do [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                                         | Retorna o objeto para o estado em que estava logo depois [**que LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) foi chamado.<br/>                             |
| [**UnlockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-unlockforprocess) (herdado do [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                   | Oposto de LockForProcess: as variáveis alocadas [**durante LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) devem ser desalocadas nesse método.<br/> |



 

## <a name="protected-methods"></a>Métodos Protegidos



|                                                                                          |                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetRegistrationPropertiesInternal**](/windows/win32/api/xapobase/nf-xapobase-cxapobase-getregistrationpropertiesinternal) | Retorna um ponteiro para a estrutura [**XAPO \_ REGISTRATION \_ PROPERTIES**](/windows/desktop/api/xapo/ns-xapo-xapo_registration_properties)S que contém as propriedades de registro com as que o XAPO foi criado.<br/> |
| [**IsLocked**](/windows/win32/api/xapobase/nf-xapobase-cxapobase-islocked)                                                   | Verifica se o XAPO está bloqueado.<br/>                                                                                                                                                |
| LONG m \_ lReferenceCount<br/>                                                       | A contagem de referência COM do objeto XAPO.<br/>                                                                                                                                       |
| [**ProcessThru**](/windows/win32/api/xapobase/nf-xapobase-cxapobase-processthru)                                             | Chamado por uma [**implementação IXAPO::P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process) quando um XAPO é desabilitado para processamento por meio de .<br/>                                                  |
| [**ValidateFormatDefault**](/windows/win32/api/xapobase/nf-xapobase-cxapobase-validateformatdefault)                         | Verifica se um formato de áudio está dentro dos intervalos padrão com suporte.<br/>                                                                                                     |
| [**ValidateFormatPair**](/windows/win32/api/xapobase/nf-xapobase-cxapobase-validateformatpair)                               | Verifica se há suporte para uma configuração de par de formato de entrada e saída em relação aos sinalizadores de propriedade XAPO.<br/>                                                            |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Classe CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase)
</dt> </dl>

 

 
