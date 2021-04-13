---
title: Funções TBS
description: O TBS fornece as funções a seguir.
ms.assetid: df2d3e36-0a27-4cc0-bcb2-709eb6bedeac
keywords:
- TBS de serviços base do TPM, funções
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1b34f2dfbe18ef2230838ff4ba9ec2241d3cc2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366380"
---
# <a name="tbs-functions"></a>Funções TBS

O TBS fornece as funções a seguir.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                       | Descrição                                                                                                                                                 |
|---------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Criação de contexto Tbsi \_**](/windows/desktop/api/Tbs/nf-tbs-tbsi_context_create)<br/>                            | Cria um identificador de contexto que pode ser usado para passar comandos para TBS.<br/>                                                                               |
| [**Tbsi \_ criar \_ atestado \_ do \_ log**](/previous-versions/windows/desktop/legacy/dn455155(v=vs.85))<br/> | Cria um atestado extraindo um TrustPoint de um log de TCG.<br/>                                                                                |
| [**Tbsi \_ GetDeviceInfo**](/windows/desktop/api/Tbs/nf-tbs-tbsi_getdeviceinfo)<br/>                                | Obtém a versão do TPM no computador.<br/>                                                                                                  |
| [**Tbsi \_ obter \_ OwnerAuth**](/windows/desktop/api/Tbs/nf-tbs-tbsi_get_ownerauth)<br/>                               | Recupera a autorização do proprietário do TPM se as informações estiverem disponíveis no registro local. <br/>                                             |
| [**Tbsi \_ obter \_ log de TCG \_**](/windows/desktop/api/Tbs/nf-tbs-tbsi_get_tcg_log)<br/>                                  | Recupera o log de configuração de inicialização mais recente do Windows (WBCL), também conhecido como log de TCG.<br/>                                                  |
| [**Tbsi \_ obter \_ log de TCG \_ \_ ex**](/windows/desktop/api/Tbs/nf-tbs-tbsi_get_tcg_log_ex)<br/>                           | Obtém o log de configuração de inicialização do Windows (WBCL), também conhecido como o log de TCG, do tipo especificado.<br/>                                          |
| [**Tbsi \_ obter \_ logs de TCG \_**](/previous-versions/windows/desktop/legacy/dn455156(v=vs.85))<br/>                                | Obtenha um ou mais WBCL (logs de configuração de inicialização) do Windows, também chamados de logs de TCG.<br/>                                                        |
| [**\_Comando de \_ presença \_ física Tbsi**](/windows/desktop/api/Tbs/nf-tbs-tbsi_physical_presence_command)<br/>     | Passa um comando ACPI de presença física por meio de TBS para o driver.<br/>                                                                               |
| [**\_Atestado de revogação Tbsi \_**](/windows/desktop/api/Tbs/nf-tbs-tbsi_revoke_attestation)<br/>                     | Invalida o PCRs se o driver ELAM detectar uma violação de política (um rootkit, por exemplo).<br/>                                                     |
| [**\_Comandos de cancelamento do Tbsip \_**](/windows/desktop/api/Tbs/nf-tbs-tbsip_cancel_commands)<br/>                        | Cancela todos os comandos pendentes para o contexto especificado.<br/>                                                                                      |
| [**\_Fechamento do contexto Tbsip \_**](/windows/desktop/api/Tbs/nf-tbs-tbsip_context_close)<br/>                            | Fecha um identificador de contexto, que libera os recursos associados ao contexto em TBS e fecha o identificador de associação usado para se comunicar com TBS.<br/> |
| [**\_Comando Tbsip enviar \_**](/windows/desktop/api/Tbs/nf-tbs-tbsip_submit_command)<br/>                          | Envia um comando Trusted Platform Module (TPM) para os serviços de base do TPM (TBS) para processamento.<br/>                                                       |



 

 

