---
description: Proteção Windows recursos adicionais em chaves do Registro
ms.assetid: 25d07e42-b5eb-4f72-b4b1-0ebb881644ba
title: Proteção Windows recursos adicionais em chaves do Registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3ea823b2075905b8f22cbc02539f058c9ad8f2ed33ed51d712cd8cb43f59d18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995016"
---
# <a name="additional-windows-resource-protection-on-registry-keys"></a>Proteção Windows recursos adicionais em chaves do Registro

## <a name="platform"></a>Plataforma

**Clientes** – Windows 7  
**Servidores** – Windows Server 2008 R2  









## <a name="feature-impact"></a>Impacto do recurso

**Gravidade –** Média  
**Frequência** – Baixa  


## <a name="description"></a>Descrição

Recursos adicionais do sistema Windows configurações da WRP (Proteção de Recursos) no Windows 7, tornando-as configurações somente leitura. A grande maioria dos recursos que recebeu proteção adicionada são chaves de servidor COM do sistema, embora alguns recursos tenham adicionado a proteção de recurso direcionada. A Microsoft alterou esses recursos para proteger o sistema e outros aplicativos contra a quebra entre si e fornecer uma plataforma consistente e estável na qual os aplicativos podem ser executados de forma confiável. No passado, os aplicativos podiam fornecer arquivos personalizados e usar o registro COM desprotegido para alterar o sistema. No caso de aplicativos mais antigos, isso pode fazer downgrade de runtimes do sistema ou alterar a interface na qual outros aplicativos precisavam funcionar corretamente. Na pior das hipóteses, essas instalações podem causar falha ou degradação do sistema ao longo do tempo. Para fornecer uma experiência melhor e uma plataforma de aplicativo mais estável, nós bloqueadas esses registros para que somente as atualizações da Microsoft pudessem alterar os componentes do sistema.

Como a maioria dos recursos alterados são chaves COM usadas pelo sistema, essa alteração não afetará a maioria dos aplicativos. Embora esperemos que a maioria dos aplicativos tenha uma experiência melhor no Windows 7 como resultado dessas alterações, um pequeno subconjunto de aplicativos pode ser afetado negativamente. As camadas de compatibilidade do aplicativo do sistema resolverão automaticamente os problemas de instalação, sempre dizendo ao aplicativo que ele foi bem-sucedido na alteração de uma configuração, mesmo que tenha falhado devido a ser um recurso protegido. Isso impede a quebra das configurações do aplicativo, mas pode causar problemas se a configuração precisar ser alterada para que o aplicativo funcione corretamente.

## <a name="manifestation"></a>Manifestação

Os aplicativos podem ter modificado essas configurações antes Windows 7. Após a instalação no Windows 7, os aplicativos podem achar que determinados recursos não funcionam mais porque as configurações não refletiram o que o aplicativo esperava.

Há dois cenários em que os aplicativos podem encontrar problemas relacionados a essa proteção adicionada:

-   Aplicativos que podem estar usando as configurações agora protegidas como um armazenamento de dados ou como um ponto de extensibilidade raro ou não intencional
-   Em casos raros, o mecanismo de detecção usado para identificar as configurações do aplicativo pode não reconhecer uma configuração específica e, portanto, a camada de mitigação de compatibilidade do aplicativo pode não ser aplicada

## <a name="mitigation"></a>Atenuação

O principal meio de mitigação é a camada de compatibilidade do aplicativo do sistema, que é aplicada automaticamente às configurações do aplicativo quando detectada. Você também pode aplicá-lo manualmente a qualquer aplicativo usando a guia de compatibilidade nas propriedades do aplicativo.

Essa camada resolve o problema interceptando operações do Registro. No caso em que o aplicativo estava tentando modificar uma configuração somente leitura (WRP), a camada sempre retorna êxito, mesmo que a configuração não tenha sido alterada. Para a maioria dos aplicativos, isso não causará problemas. No entanto, há uma possibilidade de que o aplicativo precisasse dessa configuração alterada para funcionar corretamente, que é o primeiro cenário descrito acima.

## <a name="solution"></a>Solução

Para os dois cenários identificados acima:

-   Se o aplicativo exigir que a chave seja escrita para funcionar ou usar o armazenamento de dados, não haverá outra solução além de alterar o aplicativo para que ela não seja mais gravada nesse local.
-   Se a camada de compatibilidade não foi aplicada a uma configuração, a falha de instalação deve ser detectada e oferecida para ser aplicada e executar de novo. Os aplicativos também podem ser executados no modo de compatibilidade, caso em que a camada de mitigação sempre é aplicada.

## <a name="compatibility-tests"></a>Testes de compatibilidade

Como detectar se um aplicativo tinha a mitigação de WRP aplicada a ele:

-   Windows O instalador está ciente do WRP; ele ignora automaticamente e silenciosamente as tentativas de gravar ou modificar um recurso protegido. Se o aplicativo tiver sido instalado com o instalador do Windows e o registro em log tiver sido habilitado, um aviso será registrado para cada operação de gravação de chave do Registro que foi ignorada devido a ser um recurso protegido por WRP.
-   A API do WRP incorpora SfCIsKeyProtected, que pode consultar se uma chave do Registro está protegida por WRP no sistema atual. Consulte a entrada WRP no MSDN nos links abaixo para obter informações adicionais sobre como usar essa API.

## <a name="links-to-other-resources"></a>Links para outros recursos

<dl>

[Windows Proteção de recursos](/windows/desktop/Wfp/windows-resource-protection-portal)  
</dl>

 

 
