---
description: Orca.exe é um editor de tabela de banco de dados para criar e editar Windows Installer pacotes e Mesclar módulos.
ms.assetid: 4dddc262-1271-4e00-a986-53380b957b17
title: Orca.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4647b137650bfba521dba3976ea7a1ae66451ce
ms.sourcegitcommit: 967ba3a2a618e6088cb607164a2a924530278645
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113102155"
---
# <a name="orcaexe"></a>Orca.exe

Orca.exe é um editor de tabela de banco de dados para criar e editar Windows Installer pacotes e Mesclar módulos. A ferramenta fornece uma interface gráfica para validação, destacando as entradas específicas em que ocorrem erros de validação ou avisos.

Essa ferramenta só está disponível nos [componentes SDK do Windows para desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md). Ele é fornecido como um arquivo de Orca.msi. Depois de instalar os componentes de SDK do Windows para os desenvolvedores de Windows Installer, clique duas vezes em Orca.msi para instalar o arquivo de Orca.exe.

## <a name="syntax"></a>Sintaxe

**Orca***\[\<options>\]\[\<source file>\]*

## <a name="command-line-options"></a>Opções de linha de comando

Orca.exe usa as seguintes opções de linha de comando que não diferenciam maiúsculas de minúsculas. Um delimitador de barra também pode ser usado no lugar de um traço.



| Opção | Descrição                                                 |
|--------|-------------------------------------------------------------|
| -Q     | Modo silencioso                                                  |
| -S     | <*banco de dados> esquema* \[ de dados "Orca. dat"-default\] |
| -?     | Caixa de diálogo de ajuda                                                 |



 

Orca.exe usa as seguintes opções de linha de comando que não diferenciam maiúsculas de minúsculas com módulos de mesclagem. Um delimitador de barra também pode ser usado no lugar de um traço. Ao executar uma mesclagem, os> de *origem* -f,-m e <são todos necessários.



| Opção     | Descrição                                                                |
|------------|----------------------------------------------------------------------------|
| -c         | Confirmar mesclagem no banco de dados se não houver erros.                                     |
| -!         | Confirme a mesclagem em um banco de dados, mesmo se houver erros.                       |
| -M         | <*módulo*> módulo de mesclagem para mesclar no banco de dados.                      |
| -f         | Recurso \[ : \] recurso (s) Feature2 para se conectar ao módulo de mesclagem.                |
| -r         | <*ID de diretório*> entrada de diretório para o redirecionamento de raiz do módulo.    |
| -X         | <o *diretório*> extrair arquivos para uma imagem sob o diretório.         |
| -g         | <linguagem de> de *idiomas* usada para abrir um módulo.                         |
| -l         | <arquivo de *log*> arquivo para usar como um log, acrescentar se ele já existir.      |
| -i         | <o *diretório*> extrair arquivos para a imagem de origem no diretório. |
| -CAB       | <*nome* de arquivo> extrair o gabinete msm para o arquivo.                        |
| -lfn       | Use nomes de arquivo longos durante a extração.                                 |
| -configurar | <o *nome* de arquivo> configurar o módulo usando dados de um arquivo.            |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Ferramentas de desenvolvimento Windows Installer](windows-installer-development-tools.md)
</dt> <dt>

[Versões, ferramentas e redistribuíveis liberados](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



