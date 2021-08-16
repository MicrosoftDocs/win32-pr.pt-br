---
description: O Microsoft .NET Framework oferece a capacidade de implantar aplicativos de um servidor de arquivos ou Web.
ms.assetid: 7721cd92-241f-4409-a724-c8e8768a19a9
title: Nenhuma implantação de toque
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d31f01742a1b1231171688ea15634913c56ef613c8f6ebdaf3042b4998f00a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117856535"
---
# <a name="no-touch-deployment"></a>Nenhuma implantação de toque

O Microsoft .NET Framework oferece a capacidade de implantar aplicativos de um servidor de arquivos ou Web. Essa técnica, chamada "implantação sem toque", combina o desempenho e a interatividade de um aplicativo cliente inteligente com todas as vantagens de implantação de um aplicativo Web. Para implantar seu aplicativo pela Web, clique com o botão direito do mouse na pasta que contém o executável e selecione **Propriedades**. Na guia **Compartilhamento da Web,** selecione **Compartilhar esta pasta**. Insira um alias para a pasta. Agora, o executável pode ser executado pela Web usando esse alias como o diretório em seu servidor. Para obter mais informações sobre a implantação sem toque, consulte [.NET Smart Clients e](/archive/msdn-magazine/2002/july/net-zero-deployment-security-and-versioning-models-in-the-windows-forms-engine-help-you-create-and-deploy-smart-clients) [Implantação](/documentation/?url=%2flibrary%2fdv_vstechart%2fhtml%2fvbtchno-touchdeploymentinnetframework.asp)sem toque no .NET Framework .

> [!Note]  
> Você deve ter Serviços de Informações da Internet da Microsoft (IIS) instalado em seu computador para habilitar a guia **Compartilhamento** da Web na **caixa de diálogo** Propriedades.

 

A implantação sem toque é aplicada a aplicativos habilitados para tinta da mesma maneira que qualquer outro aplicativo Windows Forms. Os exemplos fornecidos pelo SDK (Kit de Desenvolvimento de Software) do Microsoft Windows XP Tablet PC Edition incluem uma versão de implantação sem toque do exemplo declarações automáticas, na seção Amostras da Web do Ink dos exemplos. Este exemplo usa o Exemplo [de Formulário de Declarações](auto-claims-form-sample.md) Automáticas original e fornece um instalador que coloca em um compartilhamento da Web. Quando o Microsoft Internet Explorer navega para AutoClaims.exe no diretório que mapeia para o compartilhamento da Web, o aplicativo é lançado. Consulte [Exemplo da Web de implantação sem toque](no-touch-deployment-web-sample.md) para obter mais informações sobre o exemplo.

> [!Note]  
> Quando você implanta um aplicativo .NET pela Web, o aplicativo pode ser afetado pelo modelo de segurança do .NET. A [seção Segurança e Confiança](security-and-trust.md) descreve como a segurança funciona com aplicativos Web habilitados para tinta.

 

 

 