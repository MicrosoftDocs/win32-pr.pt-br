---
description: .
ms.assetid: 4199521A-58E6-4475-9B95-A724AB52969A
title: Corrigindo problemas de compatibilidade de instalação do ActiveX para usuários padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1e50ed2aa9e428164e39b377b65c418d82df1e5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103663801"
---
# <a name="fixing-activex-installation-compatibility-issues-for-standard-users"></a>Corrigindo problemas de compatibilidade de instalação do ActiveX para usuários padrão

Para desenvolver um ambiente de área de trabalho seguro, você deve mitigar as ameaças de controles ActiveX mal-intencionados e fornecer um nível apropriado de compatibilidade de aplicativos em seu ambiente. Um *controle ActiveX* é uma parte do código executável (normalmente um arquivo ocx empacotado em um arquivo de gabinete) que é instalado e executado por meio do Windows Internet Explorer. Você pode criar controles ActiveX para adicionar funcionalidade a aplicativos Web que não podem ser obtidas com facilidade usando código HTML padrão ou um script simples.

A instalação de controles ActiveX se torna um problema de compatibilidade quando a migração para o Windows 7 inclui uma transição para usuários padrão. Esse tipo de transição é uma prática recomendada comum em que os profissionais de ti movem seu ambiente para uma [conta de usuário padrão](https://support.microsoft.com/hub/4338813/windows-help). Essa transição não é um requisito para a implantação do Windows Internet Explorer 8.

## <a name="activex-control-installation"></a>Instalação do controle ActiveX

Os controles ActiveX têm um modelo simples para baixar e executar implantação. Os controles ActiveX são instalados e executados por meio do elemento de **objeto** HTML. O atributo **codebase** neste elemento informa ao Internet Explorer (usando uma URL) onde obter o controle se ele ainda não estiver instalado no computador do usuário. Nesse caso, o Internet Explorer baixa o pacote de instalação associado, executa a verificação de confiança no objeto e solicita ao usuário a permissão de instalação no Internet Explorer.

Durante a instalação, a página de renderização registra e executa o controle. Depois que o controle é instalado, todos os usuários padrão podem executar o controle. Esse mecanismo simples de distribuição e execução fornece uma maneira fácil de distribuir seus componentes para os usuários de seu aplicativo Web. Mas os usuários da conta Standard não podem instalar diretamente controles ActiveX por computador e podem precisar de privilégios de administrador para concluir a instalação.

## <a name="activex-installer-service-axis"></a>Serviço instalador do ActiveX (AXIS)

O serviço instalador do ActiveX (AXIS) permite que você implante controles ActiveX usando Política de Grupo em computadores em uma organização. Você pode configurar o AXIS por Política de Grupo configurações, que podem ser modificadas usando o Console de Gerenciamento de Política de Grupo (GPMC) ou o Editor de Política de Grupo Local.

Há duas configurações de política para o eixo:

-   A configuração de política sites de instalação aprovados para controles ActiveX consiste em uma lista de sites de instalação aprovados, que o eixo usa para determinar se um controle ActiveX pode ser instalado.
-   A configuração política de instalação do ActiveX para sites em zonas confiáveis identifica como as zonas de sites confiáveis podem ser usadas para instalar controles ActiveX.

Quando um site tenta instalar um controle ActiveX, o eixo verifica se a URL do site está listada na lista de sites de instalação aprovados ou como parte da zona de sites confiáveis. Se o site estiver em uma dessas listas, o eixo garantirá que o site atenda aos requisitos que a política define. Se o site e o controle ActiveX atenderem aos requisitos das configurações de política, o controle será instalado. Para obter mais informações, consulte [administrando o serviço instalador do ActiveX](/previous-versions/windows/it-pro/windows-7/dd631688(v=ws.10)).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Corrigindo problemas de compatibilidade em aplicativos Web usando o modo de exibição de compatibilidade](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
