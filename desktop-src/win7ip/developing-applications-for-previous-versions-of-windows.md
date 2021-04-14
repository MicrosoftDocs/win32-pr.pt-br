---
title: Desenvolvendo aplicativos para versões anteriores do Windows
description: Explica o que fazer para desenvolver aplicativos executados em versões anteriores do Windows e aproveitar a API que tem suporte com a atualização de plataforma para o Windows Vista e a atualização de plataforma para o Windows Server 2008.
ms.assetid: 9c46f894-e5cd-46a1-81c8-f63b09504735
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 299d4c61b0e2b931c3833934c843bf964fc3fa7c
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "104370836"
---
# <a name="developing-applications-for-previous-versions-of-windows"></a>Desenvolvendo aplicativos para versões anteriores do Windows

Explica o que fazer para desenvolver aplicativos executados em versões anteriores do Windows e aproveitar a API que tem suporte com a atualização de plataforma para o Windows Vista e a atualização de plataforma para o Windows Server 2008.

## <a name="required-downloads"></a>Downloads necessários

O download e a instalação dos pacotes descritos nas seções a seguir serão necessários se você quiser desenvolver aplicativos que usam a API introduzida com o SDK (Software Development Kit) do Microsoft Windows para Windows 7.

### <a name="microsoft-windows-sdk"></a>SDK do Microsoft Windows

O SDK do Windows para o Windows 7 é necessário para criar aplicativos que usam APIs com suporte com a atualização de plataforma para Windows Vista e a atualização de plataforma para o Windows Server 2008.

Para obter acesso a recursos adicionais e informações, como downloads, Postagens de fórum e o blog da equipe SDK do Windows, consulte o [SDK do Windows Developer Center](https://msdn.microsoft.com/bb980924.aspx) ( https://msdn.microsoft.com/bb980924.aspx) .

### <a name="net-framework"></a>.NET Framework

O .NET Framework 3,5 Service Pack 1 é necessário para criar aplicativos que usam APIs com suporte da atualização de plataforma para o Windows Vista e a atualização de plataforma para o Windows Server 2008.

Para obter recursos adicionais e informações, consulte o [.NET Framework Developer Center](https://msdn.microsoft.com/netframework/default.aspx) ( https://msdn.microsoft.com/netframework/default.aspx) .

### <a name="directx-sdk-required-when-using-direct3d"></a>SDK do DirectX necessário ao usar o Direct3D

Se você criar aplicativos que usam o Direct3D, o [SDK do DirectX](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/aa937788.aspx) é necessário para criar aplicativos que usam APIs com suporte da atualização da plataforma para o Windows Vista e a atualização da plataforma para o Windows Server 2008.

### <a name="update-your-development-computer"></a>Atualizar seu computador de desenvolvimento

Verifique se o computador de desenvolvimento tem todas as atualizações mais recentes do Windows Update.

Se você estiver desenvolvendo aplicativos em uma versão anterior do Windows, deverá obter a atualização da plataforma para o Windows Vista ou a atualização da plataforma para a atualização do Windows Server 2008 do Windows Update. A instalação de qualquer uma dessas atualizações permitirá que você aproveite a nova API fornecida pelo SDK do Windows para o Windows 7.

Para obter mais informações sobre como obter atualizações do Windows Update consulte o [artigo da base de dados de conhecimento sobre a atualização da plataforma para Windows Vista (KB 971644)](https://support.microsoft.com/kb/971644) ( https://support.microsoft.com/kb/971644) .

## <a name="development-environment"></a>Ambiente de desenvolvimento

### <a name="set-the-build-target-to-windows-7"></a>Definir o destino da compilação para o Windows 7

Todos os aplicativos que usam bibliotecas na atualização da plataforma para Windows Vista devem ser criados na plataforma de destino do Windows 7.

A configuração de WINVER para o valor da plataforma de destino do Windows 7 permite que você desenvolva aplicativos que usam APIs compatíveis com a atualização da plataforma para o Windows Vista ou a atualização da plataforma para o Windows Server 2008 em um computador de desenvolvimento que executa o Windows Vista.

Você pode definir a plataforma de destino para o Windows 7 em seu código-fonte ou usando a opção/D com o compilador do Visual Studio.

O exemplo a seguir mostra como definir WINVER em seu código-fonte.


```C++
#define WINVER 0x0601
```



O exemplo a seguir mostra como definir WINVER usando a opção de compilador/D.

``` syntax
/DWINVER=0x0601
```

## <a name="application-deployment"></a>Implantação do aplicativo

Se você criar seu aplicativo usando os cabeçalhos e as bibliotecas fornecidos pelo SDK do Windows para o Windows 7, as APIs com suporte serão executadas em qualquer versão do Windows que tenha a atualização de plataforma para o Windows Vista ou a atualização de plataforma para o Windows Server 2008 instalada.

> [!Note]  
> O comportamento, o desempenho ou os requisitos para algumas APIs com suporte na atualização da plataforma para o Windows Vista ou a atualização da plataforma para o Windows Server 2008 podem variar em diferentes versões do Windows. Para obter detalhes sobre uma API específica com suporte das atualizações, consulte [sobre a atualização de plataforma para o Windows Vista](platform-update-for-windows-vista-overview.md).

 

### <a name="no-redistributable-components"></a>Nenhum componente redistribuível

Seu aplicativo não precisa instalar componentes redistribuíveis, como DLLs ou outros arquivos de tempo de execução.

### <a name="requires-updated-end-user-computer"></a>Requer um computador End-User atualizado

Como a atualização de plataforma para o Windows Vista e a atualização de plataforma para Windows Server 2008 são hospedadas pelo Windows Update, os usuários finais com atualizações automáticas habilitadas têm grande probabilidade de já terem essas atualizações, bem como os Service Packs necessários.

Se o computador do usuário final não tiver a atualização de plataforma para Windows Vista ou atualização de plataforma para Windows Server 2008 instalada e seu aplicativo exigir APIs com suporte nessas atualizações, o aplicativo poderá não ser capaz de executar no computador do usuário final ou poderá encontrar erros durante a execução.

Para evitar os problemas que podem ser causados pelo computador do usuário que está desatualizado, você deseja verificar se o computador do usuário tem a atualização da plataforma para o Windows Vista ou a atualização da plataforma para a atualização do Windows Server 2008 durante a instalação do seu aplicativo. Você pode usar a [API do agente de Windows Update](/windows/desktop/Wua_Sdk/portal-client) para verificar se há atualizações instaladas no computador do usuário final. Você também pode usar a API do agente Windows Update para baixar e instalar as atualizações necessárias durante a instalação do aplicativo se o usuário final ainda não tiver instalado as atualizações.

Para obter um exemplo de um instalador que demonstra como usar a [API do agente de Windows Update](/windows/desktop/Wua_Sdk/portal-client), consulte [implantação do Direct3D 11 para desenvolvedores de jogos](../direct3darticles/direct3d11-deployment.md) no SDK do [DirectX](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/aa937788.aspx) .

Embora o exemplo do instalador do D3D11InstallHelper que é discutido na [implantação do Direct3D 11 para desenvolvedores de jogos](../direct3darticles/direct3d11-deployment.md), foi escrito para aplicativos que usam o Direct3D 11, ele fornece um bom exemplo de como interagir com a [API do agente de Windows Update](/windows/desktop/Wua_Sdk/portal-client) para iniciar e acompanhar o download e a instalação de atualizações que são hospedadas pelo Windows Update. A compilação deste exemplo pode exigir o SDK do Windows para o Windows 7. Para obter informações adicionais sobre o exemplo de D3D11InstallHelper, incluindo problemas conhecidos, consulte o [SDK do DirectX](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/aa937788.aspx) notas de versão para agosto de 2009. atualização da plataforma para Windows Vista

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Atualização da plataforma para Windows Vista](platform-update-for-windows-vista-portal.md)
</dt> <dt>

**Visões gerais**
</dt> <dt>

[Sobre a atualização da plataforma para Windows Vista](platform-update-for-windows-vista-overview.md)
</dt> <dt>

[Artigo da base de dados de conhecimento sobre a atualização da plataforma para Windows Vista (KB 971644)](https://support.microsoft.com/kb/971644)
</dt> </dl>

 

 