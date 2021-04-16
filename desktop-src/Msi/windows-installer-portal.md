---
description: Mecanismo do instalador usado para instalar aplicativos ou atualizações ou serviços executados no Windows. Configura e repara os aplicativos instalados. Grave pacotes MSI personalizados para criar uma instalação de instalação exe ou atualizar ou atualizar para um aplicativo.
ms.assetid: c90b8cbe-d7a1-44ad-ae65-80115bd55e4f
title: Windows Installer
ms.topic: article
ms.date: 05/19/2020
ms.openlocfilehash: d818a3decc7cbede527929dc3756ba2edf193421
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759367"
---
# <a name="windows-installer"></a>Windows Installer

> [!NOTE]
> Esta documentação destina-se a desenvolvedores de software que desejam usar Windows Installer para criar pacotes de instalador para aplicativos. Se você estiver procurando um redistribuível para Windows Installer 4,5 e anterior, consulte [Este artigo](windows-installer-redistributables.md). Observe que não há redistribuível para o Windows Installer 5,0. Essa versão está incluída no sistema operacional no Windows 7, no Windows Server 2008 R2 e em versões de cliente e servidor posteriores (incluindo o Windows 10).

Microsoft Windows Installer é um serviço de instalação e configuração fornecido com o Windows. O serviço do instalador permite que os clientes forneçam uma implantação corporativa melhor e fornece um formato padrão para o gerenciamento de componentes. O instalador também habilita o anúncio de aplicativos e recursos de acordo com o sistema operacional. Para obter mais informações, consulte [suporte de plataforma do anúncio](platform-support-of-advertisement.md).

Esta documentação descreve Windows Installer 5,0 e versões anteriores. Nem todos os recursos disponíveis nas versões mais recentes do Windows Installer estão disponíveis em versões anteriores. Esta documentação não descreve as versões anteriores à Windows Installer 2,0. Pacotes de instalação e patches que são criados para o Windows Installer 2,0 ainda podem ser instalados usando o Windows Installer 3,0 e posterior.

Windows Installer 3,0 e posterior, o pode instalar vários patches com uma única transação que integra o progresso, a reversão e as reinicializações da instalação. O instalador pode aplicar patches em uma ordem especificada, independentemente da ordem em que os patches são fornecidos ao sistema. A aplicação de patch usando o Windows Installer 3,0 apenas atualiza arquivos afetados pelo patch e pode ser significativamente mais rápida do que as versões anteriores do instalador. Os patches instalados com o Windows Installer 3,0 ou posterior podem ser desinstalados em qualquer ordem para deixar o estado do produto da mesma forma que o patch nunca foi instalado. Contas com privilégios de administrador podem usar a API do Windows Installer 3,0 e posterior para consultar e inventariar informações de produto, recurso, componente e patch. O instalador pode ser usado para ler, editar e substituir listas de origem para redes, URL e fontes de mídia. Os administradores podem enumerar entre os contextos de usuário e de instalação e gerenciar as listas de origem de um processo externo.

Windows Installer 4,5 e posterior podem instalar vários pacotes de instalação usando o [*processamento de transações*](t-gly.md). Se todos os pacotes na transação não puderem ser instalados com êxito ou se o usuário cancelar a instalação, o Windows Installer poderá reverter as alterações e restaurar o computador ao seu estado original. O instalador garante que todos os pacotes que pertencem a uma transação de vários pacotes estejam instalados ou que nenhum dos pacotes esteja instalado.

A partir do Windows Installer 5,0, um pacote pode ser criado para proteger novas contas, [Serviços](../services/services.md)do Windows, arquivos, pastas e chaves do registro. O pacote pode especificar um descritor de segurança que negue permissões, especifica a herança de permissões de um recurso pai ou especifica as permissões de uma nova conta. Para obter informações, consulte [Securing Resources](securing-resources-.md). O serviço Windows Installer 5,0 pode enumerar todos os componentes instalados no computador e obter o caminho de chave para o componente. Para obter mais informações, consulte [enumerando componentes](enumerating-components-.md). [Usando a configuração de serviços](using-services-configuration.md), Windows Installer pacotes 5,0 podem personalizar os serviços em um computador. Os desenvolvedores de instalação podem usar o Windows Installer 5,0 e a [criação de um único pacote](single-package-authoring.md) para desenvolver pacotes de instalação únicos capazes de instalar um aplicativo no [contexto de instalação](installation-context.md)por computador ou por usuário.

## <a name="where-applicable"></a>Quando aplicável

Windows Installer permite a instalação e a configuração eficientes de seus produtos e aplicativos em execução no Windows. O instalador fornece novos recursos para anunciar recursos sem instalá-los, instalar produtos sob demanda e adicionar personalizações do usuário.

Windows Installer 5,0 em execução no Windows Server 2012 ou no Windows 8 oferece suporte à instalação de aplicativos aprovados no Windows RT. Um pacote Windows Installer, patch ou transformação que não foi assinado pela Microsoft não pode ser instalado no Windows RT. A propriedade [**Summary do modelo**](template-summary.md) indica a plataforma que é compatível com um banco de dados de instalação e, nesse caso, deve incluir o valor do Windows RT.

Windows Installer destina-se ao desenvolvimento de aplicativos de estilo de área de trabalho.

## <a name="developer-audience"></a>Público de desenvolvedores

Esta documentação destina-se a desenvolvedores de software que desejam criar aplicativos que usam Windows Installer. Ele fornece informações gerais básicas sobre pacotes de instalação e o serviço do instalador. Ele contém descrições completas da interface de programação de aplicativos e dos elementos do banco de dados do instalador. Esta documentação também contém informações complementares para desenvolvedores que desejam usar um editor de tabela ou uma ferramenta de criação de pacote para fazer ou manter uma instalação.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

Windows Installer 5,0 está incluído no, no Windows 7, no Windows Server 2008 R2 e em versões posteriores. Não há pacotes redistribuíveis para o Windows Installer 5,0.

Versões anteriores à Windows Installer 5,0 foram lançadas com o Windows Server 2008, o Windows Vista, o Windows Server 2003, o Windows XP e o Windows 2000. [Windows Installer redistribuíveis](windows-installer-redistributables.md) estão disponíveis para o Windows Installer 4,5 e algumas versões anteriores.

* O Windows Installer 4,5 requer o Windows Server 2008, o Windows Vista, o Windows XP com Service Pack 2 (SP2) e posterior e o Windows Server 2003 com Service Pack 1 (SP1) e posterior.

* Windows Installer 4,0 requer o Windows Vista ou o Windows Server 2008. Não há nenhum redistribuível para instalar Windows Installer 4,0 em outros sistemas operacionais. Uma versão atualizada do Windows Installer 4,0, que não adiciona novos recursos, está disponível no Windows Vista com Service Pack 1 (SP1) e Windows Server 2008.

* O Windows Installer 3,1 requer o Windows Server 2003, o Windows XP ou o Windows 2000 com Service Pack 3 (SP3).

* O Windows Installer 3,0 requer o Windows Server 2003, o Windows XP ou o Windows 2000 com SP3. O Windows Installer 3,0 está incluído no Windows XP com Service Pack 2 (SP2). Ele está disponível como um pacote redistribuível para Windows 2000 Server com Service Pack 3 (SP3) e Windows 2000 Server com Service Pack 4 (SP4), Windows XP RTM e Windows XP com Service Pack 1 (SP1) e Windows Server 2003 RTM.

* O Windows Installer 2,0 está contido no Windows Server 2003 e no Windows XP.

* Windows Installer 2,0 está disponível como um pacote para instalação ou atualização para o Windows Installer 2,0 no Windows 2000. Este pacote não deve ser usado para instalar ou atualizar Windows Installer 2,0 no Windows Server 2003 e no Windows XP.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                       | Descrição                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [Roteiro](roadmap-to-windows-installer-documentation.md)<br/>                        | Um guia para Windows Installer documentação.<br/>       |
| [Visão geral](about-windows-installer.md)<br/>                                          | Informações gerais sobre o instalador.<br/>          |
| [O que há de novo no Windows Installer](what-s-new-in-windows-installer.md)<br/>           | Lista adições e alterações a Windows Installer.<br/> |
| [Referência](installer-function-reference.md)<br/>                                    | Documentação das funções de Windows Installer.<br/>     |
| [Exemplos de script de Windows Installer](windows-installer-scripting-examples.md)<br/> | Windows Installer exemplos usando script.<br/>          |



 

 

 
