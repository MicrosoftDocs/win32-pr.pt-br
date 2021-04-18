---
description: O Microsoft .NET Framework oferece a capacidade de implantar aplicativos de um servidor Web ou de arquivos.
ms.assetid: 7721cd92-241f-4409-a724-c8e8768a19a9
title: Nenhuma implantação por toque
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6567edf35dbd79256bed228de3941351bd5e7642
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "105793868"
---
# <a name="no-touch-deployment"></a>Nenhuma implantação por toque

O Microsoft .NET Framework oferece a capacidade de implantar aplicativos de um servidor Web ou de arquivos. Essa técnica, chamada de "implantação sem toque", combina o desempenho e a interatividade de um aplicativo cliente inteligente com todas as vantagens de implantação de um aplicativo Web. Para implantar seu aplicativo na Web, clique com o botão direito do mouse na pasta que contém o executável e selecione **Propriedades**. Na guia **compartilhamento na Web** , selecione **compartilhar esta pasta**. Insira um alias para a pasta. Agora, o executável pode ser executado pela Web usando esse alias como o diretório no servidor. Para obter mais informações sobre a implantação sem toque, consulte [.net Smart Clients](/archive/msdn-magazine/2002/july/net-zero-deployment-security-and-versioning-models-in-the-windows-forms-engine-help-you-create-and-deploy-smart-clients) and [in-Touch deployment in the .NET Framework](/documentation/?url=%2flibrary%2fdv_vstechart%2fhtml%2fvbtchno-touchdeploymentinnetframework.asp).

> [!Note]  
> Você deve ter o Microsoft Serviços de Informações da Internet (IIS) instalado no computador para habilitar a guia **compartilhamento da Web** na caixa de diálogo **Propriedades** .

 

A implantação não-Touch é aplicada a aplicativos habilitados para tinta da mesma maneira que qualquer outro aplicativo Windows Forms. Os exemplos fornecidos pelo Microsoft Windows XP Tablet PC Edition Software Development Kit (SDK) incluem uma versão de implantação sem toque do exemplo de declarações automáticas, na seção exemplos de tinta da Web dos exemplos. Este exemplo usa o [exemplo de formulário de declarações automáticas](auto-claims-form-sample.md) original e fornece um instalador que coloca em um compartilhamento da Web. Quando o Microsoft Internet Explorer navega para AutoClaims.exe no diretório que mapeia para o compartilhamento da Web, o aplicativo é iniciado. Consulte [exemplo da Web de implantação do-touch](no-touch-deployment-web-sample.md) para obter mais informações sobre o exemplo.

> [!Note]  
> Quando você implanta um aplicativo .NET na Web, o aplicativo pode ser afetado pelo modelo de segurança do .NET. A seção [segurança e confiança](security-and-trust.md) descreve como a segurança funciona com aplicativos Web habilitados para tinta.

 

 

 