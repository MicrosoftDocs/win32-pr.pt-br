---
description: O ambiente do AppContainer é um ambiente de execução de processo restritivo que pode ser usado para aplicativos herdados para fornecer segurança de recursos.
ms.assetid: 28498D4E-DCA4-4A85-B474-C3C328BD3022
title: AppContainer para aplicativos herdados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18e0cdf21fc4008f1da0d55edb17abaf71978f4a5384843ecff60793b3d5b19a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117784729"
---
# <a name="appcontainer-for-legacy-applications"></a>AppContainer para aplicativos herdados

O ambiente do AppContainer é um ambiente de execução de processo restritivo que pode ser usado para aplicativos herdados para fornecer segurança de recursos. Um aplicativo em execução em um AppContainer só pode acessar recursos especificamente concedidos a ele. Como resultado, os aplicativos implementados em um AppContainer não podem ser invadidos para permitir ações mal-intencionadas fora dos recursos limitados atribuídos.

## <a name="benefits-of-using-an-appcontainer-environment"></a>Benefícios do uso de um ambiente do AppContainer

O ambiente do AppContainer fornece proteção segura de aplicativos. Isso isola o aplicativo de acessar hardware, arquivos, registro, outros aplicativos, conectividade de rede e recursos de rede sem permissão específica. Recursos individuais podem ser direcionados sem expor outros recursos. Além disso, a identidade do usuário é protegida usando uma identidade exclusiva que é uma concatenação do usuário e o aplicativo e os recursos são concedidos usando um modelo de privilégio mínimo. Isso protege ainda mais contra um aplicativo representando o usuário para obter acesso a outros recursos.

Para obter mais informações sobre como usar o AppContainer para aplicativos herdados, consulte os tópicos a seguir.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                       | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Isolamento do AppContainer](appcontainer-isolation.md)<br/>             | O isolamento é a meta principal de um ambiente de execução do AppContainer. Ao isolar um aplicativo de recursos desnecessários e de outros aplicativos, as oportunidades de manipulação mal-intencionada são minimizadas. Conceder acesso com base no privilégio mínimo impede que aplicativos e usuários acessem recursos além de seus direitos. Controlar o acesso a recursos protege o processo, o dispositivo e a rede.<br/> |
| [Implementando um AppContainer](implementing-an-appcontainer.md)<br/> | Um AppContainer é implementado adicionando novas informações ao token de processo, alterando [**SeAccessCheck ()**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-seaccesscheck) para que todos os objetos de ACL (lista de controle de acesso) herdados não modificados bloqueiem solicitações de acesso de processos do AppContainer por padrão e objetos de Nova ACL que devem estar disponíveis para o AppContainers.<br/>                                                                                        |



 

 

