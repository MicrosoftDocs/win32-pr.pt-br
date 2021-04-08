---
description: Mostra os membros da classe CXAPOBase.
ms.assetid: 0791888B-7215-475B-95C8-B558A1E57783
title: Membros do CXAPOBase
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9ab63cf7e8ac6e4d0fa14ec412b53682aff2ba5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011325"
---
# <a name="cxapobase-members"></a>Membros do CXAPOBase

Mostra os membros da classe [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) .

## <a name="public-constructors"></a>Construtores públicos



|                                |                                                     |
|--------------------------------|-----------------------------------------------------|
| [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) | Constrói um objeto [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) . |



 

## <a name="public-methods"></a>Métodos públicos



|                                                                                                                        |                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddRef**](/previous-versions/windows/desktop/legacy/ee418448(v=vs.85)) (Herdado de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                                   | Incrementa a contagem de referência do objeto XAPO.<br/>                                                                                                         |
| [**CalcInputFrames**](/windows/win32/api/xapo/nf-xapo-ixapo-calcinputframes) (Herdado de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                     | Retorna o número de quadros de entrada necessários para gerar o número determinado de quadros de saída.<br/>                                                            |
| [**CalcOutputFrames**](/windows/win32/api/xapo/nf-xapo-ixapo-calcoutputframes) (Herdado de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                   | Retorna o número de quadros de saída necessários para gerar o número determinado de quadros de entrada.<br/>                                                            |
| [**Getregistrationproperties**](/windows/win32/api/xapo/nf-xapo-ixapo-getregistrationproperties) (Herdado de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo)) | Retorna as propriedades de registro de um XAPO.<br/>                                                                                                       |
| [**Initialize**](/windows/win32/api/xapo/nf-xapo-ixapo-initialize) (Herdado de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                               | Executa qualquer inicialização específica de efeito.<br/>                                                                                                          |
| [**IsInputFormatSupported**](/windows/win32/api/xapo/nf-xapo-ixapo-isinputformatsupported) (Herdado de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))       | Consulta se um formato de entrada específico tem suporte para um determinado formato de saída.<br/>                                                                            |
| [**IsOutputFormatSupported**](/windows/win32/api/xapo/nf-xapo-ixapo-isoutputformatsupported) (Herdado de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))     | Consulta se um formato de saída específico tem suporte para um determinado formato de entrada.<br/>                                                                            |
| [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) (Herdado de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                       | Notifica XAPO de que o [**processo**](/windows/win32/api/xapo/nf-xapo-ixapo-process) de formatos de fluxo será fornecido.<br/>                                                             |
| [**QueryInterface**](/previous-versions/windows/desktop/legacy/ee418457(v=vs.85)) (Herdado de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                   | Recupera o ponteiro de interface solicitado se o XAPO der suporte a ele.<br/>                                                                                    |
| [**Versão**](/previous-versions/windows/desktop/legacy/ee418458(v=vs.85)) (herdada de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                                 | Decrementa a contagem de referência do objeto XAPO e exclui o objeto se a contagem de referência cair em zero.<br/>                                             |
| [**Redefinir**](/windows/win32/api/xapo/nf-xapo-ixapo-reset) (Herdado de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                                         | Retorna o objeto para o estado em que ele estava logo após a chamada de [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) .<br/>                             |
| [**UnlockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-unlockforprocess) (Herdado de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                   | Oposto de LockForProcess: as variáveis alocadas durante [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) devem ser desalocadas nesse método.<br/> |



 

## <a name="protected-methods"></a>Métodos Protegidos



|                                                                                          |                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetRegistrationPropertiesInternal**](/windows/win32/api/xapobase/nf-xapobase-cxapobase-getregistrationpropertiesinternal) | Retorna um ponteiro para a estrutura S de [**\_ \_ Propriedades de registro XAPO**](/windows/desktop/api/xapo/ns-xapo-xapo_registration_properties)que contém as propriedades de registro às quais o XAPO foi criado.<br/> |
| [**IsLocked**](/windows/win32/api/xapobase/nf-xapobase-cxapobase-islocked)                                                   | Verifica se o XAPO está bloqueado.<br/>                                                                                                                                                |
| LReferenceCount m longo \_<br/>                                                       | A contagem de referência COM do objeto XAPO.<br/>                                                                                                                                       |
| [**ProcessThru**](/windows/win32/api/xapobase/nf-xapobase-cxapobase-processthru)                                             | Chamado por uma implementação [**IXAPO::P modelos**](/windows/win32/api/xapo/nf-xapo-ixapo-process) quando um XAPO é desabilitado para por meio do processamento.<br/>                                                  |
| [**ValidateFormatDefault**](/windows/win32/api/xapobase/nf-xapobase-cxapobase-validateformatdefault)                         | Verifica se um formato de áudio está dentro dos intervalos padrão com suporte.<br/>                                                                                                     |
| [**ValidateFormatPair**](/windows/win32/api/xapobase/nf-xapobase-cxapobase-validateformatpair)                               | Verifica se há suporte para uma configuração de par de formato de entrada e saída em relação aos sinalizadores de propriedade XAPO.<br/>                                                            |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Classe CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase)
</dt> </dl>

 

 
