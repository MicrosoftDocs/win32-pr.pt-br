---
description: As funções e estruturas de contexto de ativação são usadas com assemblies lado a lado.
ms.assetid: b53b30e0-948e-406c-9fb4-9681dc3c5670
title: Referência de contexto de ativação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72eb4bc136a95766a62bb96e67ac198f88fca905c60ba98e6bf922ce65a36389
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142579"
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
| [**FindActCtxSectionGuid**](/windows/desktop/api/Winbase/nf-winbase-findactctxsectionguid)     | Retorna dados contidos na estrutura DE DADOS COM CHAVE DE [**SEÇÃO DO ACTCTX \_ \_ \_**](/windows/win32/api/winbase/ns-winbase-actctx_section_keyed_data) que corresponde ao GUID especificado.   |
| [**FindActCtxSectionString**](/windows/desktop/api/Winbase/nf-winbase-findactctxsectionstringa) | Retorna dados contidos na estrutura DE DADOS COM CHAVE [**DE SEÇÃO DO ACTCTX \_ \_ \_**](/windows/win32/api/winbase/ns-winbase-actctx_section_keyed_data) que corresponde à cadeia de caracteres especificada. |
| [**GetCurrentActCtx**](/windows/desktop/api/Winbase/nf-winbase-getcurrentactctx)               | Retorna o contexto de ativação atual.                                                                                                                 |
| [**IsolationAwareCleanup**](/previous-versions/windows/desktop/legacy/aa375204(v=vs.85))     | Garante que a memória seja liberada quando um manifesto é carregado, descarregado e recarregado.                                                                         |
| [**QueryActCtxW**](/windows/desktop/api/Winbase/nf-winbase-queryactctxw)                       | Consulta o contexto de ativação para obter informações sobre um assembly ou arquivo.                                                                               |
| [**QueryActCtxSettingsW**](/windows/desktop/api/Winbase/nf-winbase-queryactctxsettingsw)       | Especifica o namespace e o nome do atributo que deve ser consultado.                                                                      |
| [**ReleaseActCtx**](/windows/desktop/api/Winbase/nf-winbase-releaseactctx)                     | Diminui a contagem de referência do contexto de ativação especificado.                                                                                     |
| [**ZombifyActCtx**](/windows/desktop/api/Winbase/nf-winbase-zombifyactctx)                     | Desativa o contexto de ativação especificado, mas não o desaloca.                                                                               |



 

A tabela a seguir lista as estruturas de contexto de ativação.



| Estrutura                                                                                                        | Descrição                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**INFORMAÇÕES \_ DETALHADAS \_ DO ASSEMBLY DE CONTEXTO \_ DE \_ ATIVAÇÃO**](/windows/desktop/api/Winnt/ns-winnt-activation_context_assembly_detailed_information) | Contém informações detalhadas sobre o contexto de ativação.                                                                                                                                                                                                                                                                                                                                  |
| [**INFORMAÇÕES \_ DETALHADAS \_ DO CONTEXTO DE \_ ATIVAÇÃO**](/windows/desktop/api/Winnt/ns-winnt-activation_context_detailed_information)                    | Contém informações sobre o assembly no contexto de ativação.                                                                                                                                                                                                                                                                                                                           |
| [**ÍNDICE \_ DE CONSULTA DE CONTEXTO DE \_ \_ ATIVAÇÃO**](/windows/desktop/api/Winnt/ns-winnt-activation_context_query_index)                                      | Contém o assembly dentro do contexto de ativação e o índice do arquivo dentro do assembly.                                                                                                                                                                                                                                                                                           |
| [**ACTCTX**](/windows/win32/api/winbase/ns-winbase-actctxa)                                                                                     | Contém informações que descrevem um contexto de ativação específico.                                                                                                                                                                                                                                                                                                                           |
| [**DADOS CHAVEADOS DA SEÇÃO ACTCTX \_ \_ \_**](/windows/win32/api/winbase/ns-winbase-actctx_section_keyed_data)                                            | Retorna as informações de contexto de ativação junto com o GUID ou a seção de contexto de ativação marcada por inteiro de 32 bits.                                                                                                                                                                                                                                                                   |
| [**INFORMAÇÕES \_ \_ DETALHADAS DO ARQUIVO \_ DE ASSEMBLY**](/windows/desktop/api/Winnt/ns-winnt-assembly_file_detailed_information)                              | Contém informações sobre um arquivo do assembly no contexto de ativação.                                                                                                                                                                                                                                                                                                                 |
| [**INFORMAÇÕES DE \_ NÍVEL DE EXECUTAR CONTEXTO DE \_ \_ \_ ATIVAÇÃO**](/windows/desktop/api/Winnt/ns-winnt-activation_context_run_level_information)                 | Usado pela [**função QueryActCtxW.**](/windows/desktop/api/Winbase/nf-winbase-queryactctxw)<br/> **Windows Server 2003 e Windows XP:** Essa estrutura não está disponível.<br/>                                                                                                                                                                                                                                    |
| [**ELEMENTO DE \_ CONTEXTO DE \_ COMPATIBILIDADE**](/windows/desktop/api/Winnt/ns-winnt-compatibility_context_element)                                         | Usado pela função [**QueryActCtxW**](/windows/desktop/api/Winbase/nf-winbase-queryactctxw) como parte da estrutura [**ACTIVATION CONTEXT \_ \_ COMPATIBILITY \_ INFORMATION.**](/windows/desktop/api/Winnt/ns-winnt-activation_context_compatibility_information) <br/> **Windows Server 2008 e anteriores, e Windows Vista e anteriores:** Essa estrutura não está disponível. Ele está disponível a partir do Windows Server 2008 R2 e Windows 7.<br/> |
| [**INFORMAÇÕES DE \_ \_ COMPATIBILIDADE DO CONTEXTO DE \_ ATIVAÇÃO**](/windows/desktop/api/Winnt/ns-winnt-activation_context_compatibility_information)          | Usado pela [**função QueryActCtxW.**](/windows/desktop/api/Winbase/nf-winbase-queryactctxw)<br/> **Windows Server 2008 e anteriores, e Windows Vista e anteriores:** Essa estrutura não está disponível. Ele está disponível a partir do Windows Server 2008 R2 e Windows 7.<br/>                                                                                                                                   |



 

A tabela a seguir lista enumerações de contexto de ativação.

| Enumeração                                                                       | Descrição                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NÍVEL DE EXECUTAR SOLICITADO POR ACTCTX \_ \_ \_**](/windows/desktop/api/Winnt/ne-winnt-actctx_requested_run_level)               | Descreve o nível de run solicitado do contexto de ativação. **Windows Server 2003 e Windows XP:** Essa enumeração não está disponível.<br/>                                                                                                      |
| [**TIPO DE ELEMENTO \_ DE \_ COMPATIBILIDADE ACTCTX \_**](/windows/desktop/api/Winnt/ne-winnt-actctx_compatibility_element_type) | Descreve o elemento de compatibilidade no manifesto do aplicativo. **Windows Server 2008 e anteriores, e Windows Vista e anteriores:** Essa enumeração não está disponível. Ele está disponível a partir do Windows Server 2008 R2 e Windows 7.<br/> |



 

 

