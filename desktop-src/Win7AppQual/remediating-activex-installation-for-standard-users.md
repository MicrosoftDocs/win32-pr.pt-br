---
description: corrigindo ActiveX problemas de compatibilidade de instalação para usuários padrão
ms.assetid: 4199521A-58E6-4475-9B95-A724AB52969A
title: corrigindo ActiveX problemas de compatibilidade de instalação para usuários padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d31dbcf8dfddd7e35a8a446f4b73dd1e5324cbe4695590511fa1cb220700b2c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994766"
---
# <a name="fixing-activex-installation-compatibility-issues-for-standard-users"></a>corrigindo ActiveX problemas de compatibilidade de instalação para usuários padrão

para desenvolver um ambiente de área de trabalho seguro, você deve mitigar as ameaças de controles de ActiveX mal-intencionados e fornecer um nível apropriado de compatibilidade de aplicativos em seu ambiente. um *controle de ActiveX* é uma parte do código executável (normalmente um arquivo OCX empacotado em um arquivo de gabinete) que é instalado e executado por meio do Windows Internet Explorer. você pode criar ActiveX controles para adicionar funcionalidade a aplicativos web que não podem ser obtidas com facilidade usando código HTML padrão ou um script simples.

A instalação de controles ActiveX se torna um problema de compatibilidade quando a migração para o Windows 7 inclui uma transição para usuários padrão. Esse tipo de transição é uma prática recomendada comum em que os profissionais de ti movem seu ambiente para uma [conta de usuário padrão](https://support.microsoft.com/hub/4338813/windows-help). essa transição não é um requisito para a implantação do Windows Internet Explorer 8.

## <a name="activex-control-installation"></a>ActiveX Instalação de controle

os controles de ActiveX têm um modelo simples de baixar e executar implantação. ActiveX controles são instalados e executados por meio do elemento de **objeto** HTML. O atributo **codebase** neste elemento informa ao Internet Explorer (usando uma URL) onde obter o controle se ele ainda não estiver instalado no computador do usuário. Nesse caso, o Internet Explorer baixa o pacote de instalação associado, executa a verificação de confiança no objeto e solicita ao usuário a permissão de instalação no Internet Explorer.

Durante a instalação, a página de renderização registra e executa o controle. Depois que o controle é instalado, todos os usuários padrão podem executar o controle. Esse mecanismo simples de distribuição e execução fornece uma maneira fácil de distribuir seus componentes para os usuários de seu aplicativo Web. mas os usuários da conta standard não podem instalar diretamente os controles de ActiveX por máquina e podem precisar de privilégios de administrador para concluir a instalação.

## <a name="activex-installer-service-axis"></a>ActiveX Serviço do instalador (eixo)

o serviço do instalador do ActiveX (AXIS) permite que você implante controles de ActiveX usando Política de Grupo em computadores de uma organização. Você pode configurar o AXIS por Política de Grupo configurações, que podem ser modificadas usando o Console de Gerenciamento de Política de Grupo (GPMC) ou o Editor de Política de Grupo Local.

Há duas configurações de política para o eixo:

-   a configuração de política sites de instalação aprovados para ActiveX controles consiste em uma lista de Sites de instalação aprovados, que o eixo usa para determinar se um controle de ActiveX pode ser instalado.
-   a configuração da política de instalação ActiveX para sites em zonas confiáveis identifica como as zonas de sites confiáveis podem ser usadas para instalar os controles de ActiveX.

quando um site tenta instalar um controle de ActiveX, o eixo verifica se a URL do site está listada na lista de sites de instalação aprovados ou como parte da zona de sites confiáveis. Se o site estiver em uma dessas listas, o eixo garantirá que o site atenda aos requisitos que a política define. Se o site e o controle ActiveX atenderem aos requisitos das configurações de política, o controle será instalado. para obter mais informações, consulte [administrando o serviço instalador do ActiveX](/previous-versions/windows/it-pro/windows-7/dd631688(v=ws.10)).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Corrigindo problemas de compatibilidade em aplicativos Web usando o modo de exibição de compatibilidade](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
