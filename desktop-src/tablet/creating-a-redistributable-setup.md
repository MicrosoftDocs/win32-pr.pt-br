---
description: para distribuir um aplicativo habilitado para tinta em computadores que não executam o Windows Vista ou o Windows XP Tablet PC Edition 2005 (ou seja, computadores que executam o Windows XP, Windows Server 2003 ou Windows 2000), você deve incluir os módulos de mesclagem necessários na sua configuração.
ms.assetid: 97515703-0bf4-4230-ae35-181b48b70c40
title: Criando uma instalação redistribuível
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80bdd63a00f1f4245ea83173e1a7e609094fe30e5357f5e1ebf3d6da63182cde
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119936866"
---
# <a name="creating-a-redistributable-setup"></a>Criando uma instalação redistribuível

para distribuir um aplicativo habilitado para tinta em computadores que não executam o Windows Vista ou o Windows XP Tablet PC Edition 2005 (ou seja, computadores que executam o Windows XP, Windows Server 2003 ou Windows 2000), você deve incluir os módulos de mesclagem necessários na sua configuração.

o módulo de mesclagem Mstpcrt. msm inclui todos os arquivos, recursos, entradas de registro e lógica de instalação necessária para Windows Installer instalar os arquivos compartilhados que outras plataformas exigem para executar aplicativos não gerenciados desenvolvidos para o Tablet PC. Mstpcrt. msm é consumido por arquivos Windows Installer (.msi). Para aplicativos que usam o objeto [**InkDivider**](inkdivider-class.md) , você também deve redistribuir InkDiv. msm. Para aplicativos que usam componentes gerenciados, você também deve incluir os arquivos do módulo de mesclagem para esses componentes gerenciados.

a tabela a seguir descreve os arquivos do módulo de mesclagem fornecidos com o SDK (Software Development Kit) do Windows XP Tablet PC Edition.



| Módulo de mesclagem redistribuível | Descrição                                                                                                                    | Arquivos                                                       |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| InkDiv. msm<br/>        | Instala a versão não gerenciada do objeto [**InkDivider**](inkdivider-class.md) .<br/>                                | InkDiv.dll<br/>                                       |
| Mstpcrt. msm<br/>       | Instala os componentes não gerenciados da plataforma Tablet PC versão 1,0.<br/>                                            | Gdiplus.dll, InkEd.dll, Tpcps.dll Wisptis.exe<br/>   |
| Msvcp60. msm<br/>       | instala componentes do tempo de execução do Microsoft Visual C++.<br/>                                                            | Msvcp60.dll<br/>                                      |
| Msvcrt. msm<br/>        | Instala componentes do tempo de execução do Microsoft Visual C.<br/>                                                              | Msvcrt.dll<br/>                                       |
| Tpcman17. msm<br/>      | Instala os componentes gerenciados do tempo de execução da plataforma do Tablet PC. Requer que o arquivo mstpcrt. msm esteja instalado.<br/> | Microsoft.Ink.dll, Microsoft.Ink.resources.dll<br/>   |
| iaCOM. msm<br/>         | Instala os componentes de automação da API do InkAnalysis.<br/>                                                          | IACom.dll<br/>                                        |
| IACore. msm<br/>        | Instala os componentes da classe base da API do InkAnalysis.<br/>                                                          | IACore.dll<br/> IALoader.dll<br/>               |
| IAWinFrm. msm<br/>      | Instala os componentes da biblioteca gerenciada da API do InkAnalysis.<br/>                                                     | Microsoft.Ink.Analysis.dll<br/>                       |
| IAWinFX. msm<br/>       | instala os componentes Windows Presentation Foundation da API InkAnalysis.<br/>                                     | IAWinFX.dll<br/>                                      |
| Journal. msm<br/>       | Instala os componentes do leitor de diário.<br/>                                                                             | Journal.dll<br/> Microsoft.ink.journal.dll<br/> |
| rtscom. msm<br/>        | Instala os componentes de automação do namespace StylusInput.<br/>                                                    | Rtscom.dll<br/>                                       |



 

> [!Note]  
> para usar a funcionalidade do Microsoft .NET Framework incluído em módulos de mesclagem para componentes gerenciados, você deve ter instalado o Service Pack 2 da estrutura no computador de destino.

 

## <a name="reduced-feature-set"></a>Conjunto de recursos reduzidos

Os aplicativos habilitados para tinta tratam eventos de mouse como movimentos de caneta para simular o trabalho com uma caneta eletrônica. Os usuários podem adicionar tinta, apagar tinta e salvar documentos à tinta. no entanto, o reconhecimento e os gestos não estão disponíveis para usuários diferentes daqueles que executam o Windows XP Tablet PC Edition.

Mstpcrt. msm não inclui Windows diário ou painel de entrada do Tablet PC.

o objeto [**PenInputPanel**](peninputpanel-class.md) não funciona em nenhum sistema operacional além do Windows XP Tablet PC Edition.

## <a name="deployment"></a>Implantação

> [!Note]  
> Se seu aplicativo usar código gerenciado, você também deverá implantar a estrutura. A estrutura deve ser instalada antes que os assemblies gerenciados do Tablet PC sejam instalados.

 

para incluir Mstpcrt. msm em um projeto de instalação Microsoft Visual Studio .net:

1.  Na Gerenciador de Soluções, selecione seu projeto de instalação.
2.  no menu Project, clique em **adicionar** e, em seguida, clique em **módulo de mesclagem**.
    > [!Note]  
    > Você também pode acessar a caixa de diálogo **Adicionar módulos** clicando com o botão direito do mouse no nome do projeto do instalador no Gerenciador de soluções, clicando em **Adicionar** e, em seguida, selecionando **módulo de mesclagem**.

     

3.  Na caixa de diálogo **Adicionar módulos** , navegue até e selecione **Mstpcrt. msm**.
4.  Clique em **Abrir**.

Mstpcrt. msm é adicionado ao seu projeto de instalação e aparece na janela Gerenciador de Soluções.

Windows O instalador adiciona os arquivos contidos no módulo de mesclagem à pasta arquivos de programas. Para usar esses arquivos, os usuários finais devem estar conectados com uma conta que tenha acesso à pasta arquivos de programas.

> [!Note]  
> Você deve adicionar ações de ação [SelfRegModules](../msi/selfregmodules-action.md) e [SelfUnregModules](../msi/selfunregmodules-action.md) à sequência de instalação. As ações de ação [MsiPublishAssemblies](../msi/msipublishassemblies-action.md) e [MsiUnpublishAssemblies](/windows/desktop/Msi/msiunpublishassemblies-action) recebem sua ordem na sequência de instalação dessas ações.

 

 

