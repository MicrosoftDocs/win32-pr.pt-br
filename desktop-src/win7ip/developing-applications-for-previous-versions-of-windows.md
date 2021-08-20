---
title: Desenvolvendo aplicativos para versões anteriores do Windows
description: Explica o que fazer para desenvolver aplicativos executados em versões anteriores do Windows e aproveitar a API com suporte com a Atualização de Plataforma para Windows Vista e a Atualização de Plataforma para Windows Server 2008.
ms.assetid: 9c46f894-e5cd-46a1-81c8-f63b09504735
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7afbb999faf934ae621f80a824eca0289ff3df705ed11d7cfd161935c944947f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119549476"
---
# <a name="developing-applications-for-previous-versions-of-windows"></a>Desenvolvendo aplicativos para versões anteriores do Windows

Explica o que fazer para desenvolver aplicativos executados em versões anteriores do Windows e aproveitar a API com suporte com a Atualização de Plataforma para Windows Vista e a Atualização de Plataforma para Windows Server 2008.

## <a name="required-downloads"></a>Downloads necessários

O download e a instalação dos pacotes descritos nas seções a seguir são necessários se você quiser desenvolver aplicativos que usam a API que são introduzidos com o SDK (Software Development Kit) do Microsoft Windows para Windows 7.

### <a name="microsoft-windows-sdk"></a>SDK Windows Microsoft

O SDK do Windows para Windows 7 é necessário para criar aplicativos que usam APIs com suporte com a Atualização de Plataforma para Windows Vista e a Atualização de Plataforma para Windows Server 2008.

Para obter acesso a recursos e informações adicionais, como downloads, postagens no fórum e o blog da equipe do SDK do Windows, consulte o Windows Centro de Desenvolvedores do [SDK](https://msdn.microsoft.com/bb980924.aspx) do Windows ( https://msdn.microsoft.com/bb980924.aspx) .

### <a name="net-framework"></a>.NET Framework

O .NET Framework 3.5 Service Pack 1 é necessário para criar aplicativos que usam APIs com suporte na Atualização de Plataforma para Windows Vista e na Atualização da Plataforma para Windows Server 2008.

Para obter mais recursos e informações, consulte [o .NET Framework Developer Center](https://msdn.microsoft.com/netframework/default.aspx) ( https://msdn.microsoft.com/netframework/default.aspx) .

### <a name="directx-sdk-required-when-using-direct3d"></a>SDK do DirectX necessário ao usar o Direct3D

Se você criar aplicativos que usam o Direct3D, o [SDK](/previous-versions/windows/apps/hh452744(v=win.10)) do DirectX ( será necessário para criar aplicativos que usam APIs com suporte na Atualização de Plataforma para o Windows Vista e na Atualização da Plataforma https://msdn.microsoft.com/directx/aa937788.aspx) para Windows Server 2008.

### <a name="update-your-development-computer"></a>Atualizar seu computador de desenvolvimento

Verifique se o computador de desenvolvimento tem todas as atualizações mais recentes do Windows Update.

Se você estiver desenvolvendo aplicativos em uma versão anterior do Windows, deverá obter a Atualização da Plataforma para o Windows Vista ou a atualização da plataforma para o Windows Server 2008 da atualização Windows Update. A instalação de qualquer uma dessas atualizações permitirá que você aproveite a nova API fornecida pelo SDK do Windows para Windows 7.

Para obter mais informações sobre como obter atualizações do Windows Update, consulte o artigo da Base de Dados de Conhecimento sobre a Atualização de Plataforma para [Windows Vista (KB 971644)](https://support.microsoft.com/kb/971644) ( https://support.microsoft.com/kb/971644) .

## <a name="development-environment"></a>Ambiente de desenvolvimento

### <a name="set-the-build-target-to-windows-7"></a>Definir o destino de build como Windows 7

Todos os aplicativos que usam bibliotecas na Atualização de Plataforma para Windows Vista devem ser construídos na plataforma de destino Windows 7.

Definir WINVER como o valor da plataforma de destino do Windows 7 permite que você desenvolva aplicativos que usam APIs com suporte com a Atualização de Plataforma para Windows Vista ou a Atualização de Plataforma para o Windows Server 2008 em um computador de desenvolvimento executando o Windows Vista.

Você pode definir a plataforma de destino como Windows 7 no código-fonte ou usando a opção /D com o compilador Visual Studio aplicativo.

O exemplo a seguir mostra como definir WINVER em seu código-fonte.


```C++
#define WINVER 0x0601
```



O exemplo a seguir mostra como definir WINVER usando a opção do compilador /D.

``` syntax
/DWINVER=0x0601
```

## <a name="application-deployment"></a>Implantação do aplicativo

Se você criar seu aplicativo usando os headers e bibliotecas fornecidos pelo SDK do Windows para o Windows 7, as APIs com suporte serão executados em qualquer versão do Windows que tenha a Atualização de Plataforma para Windows Vista ou a Atualização da Plataforma para o Windows Server 2008 instalada.

> [!Note]  
> O comportamento, o desempenho ou os requisitos para algumas APIs que têm suporte com a Atualização de Plataforma para Windows Vista ou a Atualização de Plataforma para Windows Server 2008 podem variar entre diferentes versões do Windows. Para obter detalhes sobre uma API específica com suporte nas atualizações, consulte [About Platform Update for Windows Vista](platform-update-for-windows-vista-overview.md).

 

### <a name="no-redistributable-components"></a>Nenhum componente redistribuível

Seu aplicativo não precisa instalar componentes redistribuíveis, como DLLs ou outros arquivos em tempo de executar.

### <a name="requires-updated-end-user-computer"></a>Requer um computador End-User atualizado

Como a Atualização de Plataforma para o Windows Vista e a Atualização de Plataforma para o Windows Server 2008 são hospedadas pela Atualização do Windows, os usuários finais com atualizações automáticas habilitadas provavelmente já terão essas atualizações, bem como os service packs necessários.

Se o computador do usuário final não tiver a Atualização de Plataforma para Windows Vista ou Atualização de Plataforma para o Windows Server 2008 instalada e seu aplicativo exigir APIs com suporte com essas atualizações, seu aplicativo poderá não ser executado no computador do usuário final ou poderá encontrar erros durante a execução.

Para evitar os problemas que podem ser causados pelo computador do usuário estar desajustado, você deseja verificar se o computador do usuário tem a atualização de plataforma para o Windows Vista ou a atualização de plataforma para o Windows Server 2008 atualização durante a instalação do aplicativo. Você pode usar a [API Windows Update Agent](/windows/desktop/Wua_Sdk/portal-client) para verificar se há atualizações instaladas no computador do usuário final. Você também pode usar Windows API do Agente de Atualização para baixar e instalar as atualizações necessárias durante a instalação do aplicativo se o usuário final ainda não tiver instalado as atualizações.

Para ver um exemplo de um instalador que demonstra como usar a API do agente de [atualização do Windows](/windows/desktop/Wua_Sdk/portal-client), consulte Implantação do [Direct3D 11 para](../direct3darticles/direct3d11-deployment.md) desenvolvedores de jogos no [SDK](/previous-versions/windows/apps/hh452744(v=win.10)) do DirectX ( https://msdn.microsoft.com/directx/aa937788.aspx) .

Embora o exemplo do instalador D3D11InstallHelper discutido na Implantação do [Direct3D 11](../direct3darticles/direct3d11-deployment.md)para Desenvolvedores de Jogos tenha sido escrito para aplicativos que usam o Direct3D 11, ele fornece um bom exemplo de como interagir com [a API](/windows/desktop/Wua_Sdk/portal-client) do Agente de Atualização do Windows para iniciar e acompanhar o download e a instalação de atualizações hospedadas pelo Windows Update. Compilar este exemplo pode exigir o Windows SDK para Windows 7. Para obter informações adicionais sobre o exemplo D3D11InstallHelper, incluindo problemas conhecidos, consulte o [SDK](/previous-versions/windows/apps/hh452744(v=win.10)) do DirectX ( Notas sobre a versão de agosto de https://msdn.microsoft.com/directx/aa937788.aspx) 2009.Platform Update para Windows Vista

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Atualização de plataforma para Windows Vista](platform-update-for-windows-vista-portal.md)
</dt> <dt>

**Visões gerais**
</dt> <dt>

[Sobre a Atualização de Plataforma para Windows Vista](platform-update-for-windows-vista-overview.md)
</dt> <dt>

[Artigo da Base de Dados de Conhecimento sobre a Atualização da Plataforma Windows Vista (KB 971644)](https://support.microsoft.com/kb/971644)
</dt> </dl>

 

 