---
description: As funções e estruturas de contexto de ativação são usadas com assemblies lado a lado.
ms.assetid: b53b30e0-948e-406c-9fb4-9681dc3c5670
title: Referência de contexto de ativação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d6f8225b4db8b22227edf2b779ed9e1b50da7a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010985"
---
# <a name="activation-context-reference"></a>Referência de contexto de ativação

As funções e estruturas de contexto de ativação são usadas com assemblies lado a lado.

A tabela a seguir lista as funções de contexto de ativação.



| Função                                                   | Descrição                                                                                                                                             |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ActivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-activateactctx)                   | Ativa o contexto de ativação especificado.                                                                                                             |
| [**AddRefActCtx**](/windows/desktop/api/Winbase/nf-winbase-addrefactctx)                       | Incrementa a contagem de referência do contexto de ativação especificado.                                                                                     |
| [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa)                       | Cria um contexto de ativação.                                                                                                                          |
| [**DeactivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-deactivateactctx)               | Desativa o contexto de ativação especificado.                                                                                                           |
| [**FindActCtxSectionGuid**](/windows/desktop/api/Winbase/nf-winbase-findactctxsectionguid)     | Retorna os dados contidos na estrutura de [**\_ dados com \_ chave \_ da seção ACTCTX**](/windows/win32/api/winbase/ns-winbase-actctx_section_keyed_data) que corresponde ao GUID especificado.   |
| [**FindActCtxSectionString**](/windows/desktop/api/Winbase/nf-winbase-findactctxsectionstringa) | Retorna os dados contidos na estrutura de [**\_ dados com \_ chave \_ da seção ACTCTX**](/windows/win32/api/winbase/ns-winbase-actctx_section_keyed_data) que corresponde à cadeia de caracteres especificada. |
| [**GetCurrentActCtx**](/windows/desktop/api/Winbase/nf-winbase-getcurrentactctx)               | Retorna o contexto de ativação atual.                                                                                                                 |
| [**IsolationAwareCleanup**](/previous-versions/windows/desktop/legacy/aa375204(v=vs.85))     | Garante que a memória seja liberada quando um manifesto for carregado, descarregado e recarregado.                                                                         |
| [**QueryActCtxW**](/windows/desktop/api/Winbase/nf-winbase-queryactctxw)                       | Consulta o contexto de ativação para obter informações sobre um assembly ou arquivo.                                                                               |
| [**QueryActCtxSettingsW**](/windows/desktop/api/Winbase/nf-winbase-queryactctxsettingsw)       | Especifica o namespace e o nome do atributo que deve ser consultado.                                                                      |
| [**ReleaseActCtx**](/windows/desktop/api/Winbase/nf-winbase-releaseactctx)                     | Decrementa a contagem de referência do contexto de ativação especificado.                                                                                     |
| [**ZombifyActCtx**](/windows/desktop/api/Winbase/nf-winbase-zombifyactctx)                     | Desativa o contexto de ativação especificado, mas não o desaloca.                                                                               |



 

A tabela a seguir lista as estruturas de contexto de ativação.



| Estrutura                                                                                                        | Description                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ informações detalhadas do assembly de contexto de \_ ativação \_**](/windows/desktop/api/Winnt/ns-winnt-activation_context_assembly_detailed_information) | Contém informações detalhadas sobre o contexto de ativação.                                                                                                                                                                                                                                                                                                                                  |
| [**\_ \_ informações detalhadas do contexto de ativação \_**](/windows/desktop/api/Winnt/ns-winnt-activation_context_detailed_information)                    | Contém informações sobre o assembly no contexto de ativação.                                                                                                                                                                                                                                                                                                                           |
| [**\_índice de \_ consulta do contexto de ativação \_**](/windows/desktop/api/Winnt/ns-winnt-activation_context_query_index)                                      | Contém o assembly dentro do contexto de ativação e o índice do arquivo dentro do assembly.                                                                                                                                                                                                                                                                                           |
| [**ACTCTX**](/windows/win32/api/winbase/ns-winbase-actctxa)                                                                                     | Contém informações que descrevem um contexto de ativação específico.                                                                                                                                                                                                                                                                                                                           |
| [**\_dados com \_ chave da seção ACTCTX \_**](/windows/win32/api/winbase/ns-winbase-actctx_section_keyed_data)                                            | Retorna as informações do contexto de ativação juntamente com a seção GUID ou de contexto de ativação marcada como inteiro de 32 bits.                                                                                                                                                                                                                                                                   |
| [**\_ \_ informações detalhadas do arquivo de assembly \_**](/windows/desktop/api/Winnt/ns-winnt-assembly_file_detailed_information)                              | Contém informações sobre um arquivo do assembly no contexto de ativação.                                                                                                                                                                                                                                                                                                                 |
| [**\_informações de \_ nível de execução do contexto de ativação \_ \_**](/windows/desktop/api/Winnt/ns-winnt-activation_context_run_level_information)                 | Usado pela função [**QueryActCtxW**](/windows/desktop/api/Winbase/nf-winbase-queryactctxw) .<br/> **Windows Server 2003 e Windows XP:** Esta estrutura não está disponível.<br/>                                                                                                                                                                                                                                    |
| [**\_elemento de contexto de compatibilidade \_**](/windows/desktop/api/Winnt/ns-winnt-compatibility_context_element)                                         | Usado pela função [**QueryActCtxW**](/windows/desktop/api/Winbase/nf-winbase-queryactctxw) como parte da estrutura de [**\_ informações de \_ compatibilidade \_ do contexto de ativação**](/windows/desktop/api/Winnt/ns-winnt-activation_context_compatibility_information) . <br/> **Windows Server 2008 e anterior, e Windows Vista e anterior:** Esta estrutura não está disponível. Ele está disponível a partir do Windows Server 2008 R2 e do Windows 7.<br/> |
| [**\_informações de \_ compatibilidade do contexto de ativação \_**](/windows/desktop/api/Winnt/ns-winnt-activation_context_compatibility_information)          | Usado pela função [**QueryActCtxW**](/windows/desktop/api/Winbase/nf-winbase-queryactctxw) .<br/> **Windows Server 2008 e anterior, e Windows Vista e anterior:** Esta estrutura não está disponível. Ele está disponível a partir do Windows Server 2008 R2 e do Windows 7.<br/>                                                                                                                                   |



 

A tabela a seguir lista as enumerações de contexto de ativação.

| Enumeração                                                                       | Descrição                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_nível de \_ execução \_ solicitado ACTCTX**](/windows/desktop/api/Winnt/ne-winnt-actctx_requested_run_level)               | Descreve o nível de execução solicitado do contexto de ativação. **Windows Server 2003 e Windows XP:** Esta enumeração não está disponível.<br/>                                                                                                      |
| [**\_tipo de \_ elemento de compatibilidade ACTCTX \_**](/windows/desktop/api/Winnt/ne-winnt-actctx_compatibility_element_type) | Descreve o elemento de compatibilidade no manifesto do aplicativo. **Windows Server 2008 e anterior, e Windows Vista e anterior:** Esta enumeração não está disponível. Ele está disponível a partir do Windows Server 2008 R2 e do Windows 7.<br/> |



 

 

