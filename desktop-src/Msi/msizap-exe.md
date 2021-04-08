---
description: O Msizap.exe é um utilitário de linha de comando que remove todas as informações de Windows Installer de um produto ou de todos os produtos instalados em um computador. Os produtos instalados pelo instalador podem falhar ao funcionar depois de usar o Msizap.
ms.assetid: 0debb8ab-3ae7-447e-84fc-0466ec1b2f26
title: Msizap.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a89f2287443bc442ee767b01e975d6bcc118c1d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010832"
---
# <a name="msizapexe"></a>Msizap.exe

O Msizap.exe é um utilitário de linha de comando que remove todas as informações de Windows Installer de um produto ou de todos os produtos instalados em um computador. Os produtos instalados pelo instalador podem falhar ao funcionar depois de usar o Msizap.

No Windows 2000 e no Windows XP, são necessários privilégios administrativos para usar Msizap.exe.

Essa ferramenta só está disponível nos [componentes SDK do Windows para desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md) e não deve ser redistribuída. Use a versão recente do Msizap.exe (versão 3.1.4000.2726 ou superior) que está disponível na SDK do Windows componentes para Windows Installer desenvolvedores para Windows Vista ou superior. Versões menores do Msizap.exe podem remover informações sobre todas as atualizações que foram aplicadas a outros aplicativos no computador do usuário. Se essas informações forem removidas, talvez esses outros aplicativos precisem ser removidos e reinstalados para receber atualizações adicionais.

## <a name="syntax"></a>Syntax

**Msizap T**_\[ wa! \] {código do produto}_

**Msizap T**_\[ wa! \] <msi package>_

**\* *** Msizap \[ WA! \]* **Produtos**

**Msizap PWSA?!**

## <a name="command-line-options"></a>Opções de linha de comando

Msizap.exe usa opções de linha de comando que não diferenciam maiúsculas de minúsculas mostradas na tabela a seguir.



| Opção | Descrição                                                                                                                                                                                                                                                   |
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*     | Remove todas as pastas de Windows Installer e chaves do registro, ajusta as contagens de DLL compartilhadas e interrompe Windows Installer serviço. Também remove a chave In-Progress e informações de reversão.                                                                           |
| um      | Só altera ACLs para controle total de administrador para qualquer remoção especificada.                                                                                                                                                                                            |
| g      | Para todos os usuários, o Remove todos os arquivos de dados de Windows Installer em cache que ficaram órfãos.                                                                                                                                                                       |
| p      | Remove a chave de In-Progress.                                                                                                                                                                                                                                  |
| s      | Remove informações de reversão.                                                                                                                                                                                                                                 |
| t      | Remove todas as informações do código de produto especificado. Ao usar essa opção, coloque o código do produto entre chaves. Essa opção pode ser usada com o caminho completo para o arquivo. msi ou com o código do produto.                                        |
| w      | Remove informações de Windows Installer para todos os usuários. Quando essa opção não é definida, somente as informações do usuário atual são removidas. O uso dessa opção requer que o perfil do usuário seja carregado para que o hive do registro por usuário do usuário esteja disponível. |
| ?      | Ajuda detalhada.                                                                                                                                                                                                                                                 |
| !      | Força uma resposta ' Sim ' a qualquer prompt.                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Versões, ferramentas e redistribuíveis liberados](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



