---
description: .
ms.assetid: 25d07e42-b5eb-4f72-b4b1-0ebb881644ba
title: Proteção de Recursos do Windows adicionais em chaves do registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb048a45324e52c9b9319f52f95b64361b95bbfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764030"
---
# <a name="additional-windows-resource-protection-on-registry-keys"></a>Proteção de Recursos do Windows adicionais em chaves do registro

## <a name="platform"></a>Plataforma

**Clientes** -Windows 7  
**Servidores** -Windows Server 2008 R2  









## <a name="feature-impact"></a>Impacto do recurso

**Severidade** -média  
**Frequência** -baixa  


## <a name="description"></a>Descrição

Recursos adicionais do sistema adicionam configurações de Proteção de Recursos do Windows (WRP) no Windows 7, tornando-as configurações somente leitura. A grande maioria dos recursos que receberam proteção adicional são as chaves de servidor COM do sistema, embora alguns recursos tenham adicionado a proteção de recursos direcionada. A Microsoft alterou esses recursos para proteger o sistema e outros aplicativos de dividir uns aos outros e fornecer uma plataforma estável e consistente na qual os aplicativos podem ser executados de forma confiável. No passado, os aplicativos podiam fornecer arquivos personalizados e usar o registro COM desprotegido para alterar o sistema. No caso de aplicativos mais antigos, isso pode fazer o downgrade de tempos de execução do sistema ou alterar a interface na qual outros aplicativos precisavam funcionar corretamente. Na pior das hipóteses, essas instalações poderiam causar falha ou degradação do sistema ao longo do tempo. Para fornecer uma experiência melhor e uma plataforma de aplicativo mais estável, bloqueamos esses registros para que apenas as atualizações da Microsoft pudessem alterar os componentes do sistema.

Como a maioria dos recursos alterados são chaves COM usadas pelo sistema, essa alteração não afetará a maioria dos aplicativos. Embora esperamos que a maioria dos aplicativos tenha uma experiência melhor no Windows 7 como resultado dessas alterações, um pequeno subconjunto de aplicativos pode ser afetado negativamente. As camadas de compatibilidade de aplicativos do sistema resolverão automaticamente os problemas de instalação, sempre informando ao aplicativo que ele teve êxito na alteração de uma configuração, mesmo que ela tenha falhado devido a um recurso protegido. Isso impede que as configurações de aplicativo sejam interrompidas, mas podem causar problemas se a configuração precisar ser alterada para que o aplicativo funcione corretamente.

## <a name="manifestation"></a>Manifestação

Os aplicativos podem ter modificado essas configurações antes do Windows 7. Ao instalar no Windows 7, os aplicativos podem encontrar determinados recursos que não funcionam mais porque as configurações não refletiram o que o aplicativo esperava.

Há dois cenários em que os aplicativos podem encontrar problemas relacionados a essa proteção adicional:

-   Aplicativos que podem ter usado as configurações agora protegidas como um armazenamento de dados ou como um ponto de extensibilidade raro ou indesejado
-   Em casos raros, o mecanismo de detecção usado para identificar as configurações do aplicativo pode não reconhecer uma configuração específica e, portanto, a camada de mitigação da compatibilidade de aplicativos pode não ser aplicada

## <a name="mitigation"></a>Atenuação

O principal meio de mitigação é a camada de compatibilidade de aplicativos do sistema, que é aplicada automaticamente às configurações do aplicativo quando detectada. Você também pode aplicá-lo manualmente a qualquer aplicativo usando a guia Compatibilidade nas propriedades do aplicativo.

Essa camada resolve o problema interceptando operações de registro. No caso em que o aplicativo estava tentando modificar uma configuração somente leitura (WRP), a camada sempre retorna êxito, embora a configuração não tenha sido realmente alterada. Para a maioria dos aplicativos, isso não causará nenhum problema. No entanto, há uma possibilidade de que o aplicativo precise que a configuração seja alterada para funcionar corretamente, que é o primeiro cenário descrito acima.

## <a name="solution"></a>Solução

Para os dois cenários identificados acima:

-   Se o aplicativo exigir que a chave seja gravável para poder funcionar ou usar o armazenamento de dados, não haverá nenhuma solução diferente de alterar o aplicativo para que ele não grave mais nesse local.
-   Se a camada de compatibilidade não tiver sido aplicada a uma configuração, a falha de instalação deverá ser detectada e executada novamente. Os aplicativos também podem ser executados no modo de compatibilidade. nesse caso, a camada de mitigação sempre é aplicada.

## <a name="compatibility-tests"></a>Testes de compatibilidade

Como detectar se um aplicativo tinha mitigação de WRP aplicada a ele:

-   Windows Installer está ciente da WRP; Ele ignora automaticamente e silenciosamente as tentativas de gravar ou modificar um recurso protegido. Se o aplicativo tiver sido instalado com Windows Installer e o registro em log tiver sido habilitado, um aviso será registrado para cada operação de gravação da chave do registro que foi ignorada porque ele é um recurso protegido por WRP.
-   A API WRP incorpora SfCIsKeyProtected, que pode consultar se uma chave do registro é protegida por WRP no sistema atual. Consulte a entrada WRP no MSDN nos links abaixo para obter informações adicionais sobre como usar essa API.

## <a name="links-to-other-resources"></a>Links para outros recursos

<dl>

[Proteção de Recursos do Windows](/windows/desktop/Wfp/windows-resource-protection-portal)  
</dl>

 

 
