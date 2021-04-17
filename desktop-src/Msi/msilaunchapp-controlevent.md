---
description: Esse evento de controle executa um arquivo especificado. Se o arquivo não existir ou se o evento falhar, Windows Installer registrará o erro no log detalhado sem exibir uma caixa de diálogo contendo uma mensagem de erro.
ms.assetid: a185c5a1-6584-4916-967a-313e6b7cf97c
title: MsiLaunchApp ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 298867868a80eb2cb831a2304325d14355adc669
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748150"
---
# <a name="msilaunchapp-controlevent"></a><span data-ttu-id="1fa0b-104">MsiLaunchApp ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="1fa0b-104">MsiLaunchApp ControlEvent</span></span>

<span data-ttu-id="1fa0b-105">Esse evento de controle executa um arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="1fa0b-105">This control event runs a specified file.</span></span> <span data-ttu-id="1fa0b-106">Se o arquivo não existir ou se o evento falhar, Windows Installer registrará o erro no log detalhado sem exibir uma caixa de diálogo contendo uma mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="1fa0b-106">If the file does not exist, or if the event fails, Windows Installer logs the error in the verbose log without displaying a dialog box containing an error message.</span></span>

<span data-ttu-id="1fa0b-107">**[Windows Installer 4,5 ou anterior](not-supported-in-windows-installer-4-5.md):** Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="1fa0b-107">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="1fa0b-108">Esse ControlEvent, está disponível a partir do Windows Installer 5,0.</span><span class="sxs-lookup"><span data-stu-id="1fa0b-108">This ControlEvent is available beginning with Windows Installer 5.0.</span></span>

## <a name="published-by"></a><span data-ttu-id="1fa0b-109">Publicada por</span><span class="sxs-lookup"><span data-stu-id="1fa0b-109">Published By</span></span>

<span data-ttu-id="1fa0b-110">Esse ControlEvent, é publicado pelo instalador.</span><span class="sxs-lookup"><span data-stu-id="1fa0b-110">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="1fa0b-111">Argumento</span><span class="sxs-lookup"><span data-stu-id="1fa0b-111">Argument</span></span>

<span data-ttu-id="1fa0b-112">Os campos do valor do argumento são delimitados por espaços.</span><span class="sxs-lookup"><span data-stu-id="1fa0b-112">The fields of the argument value are delimited by spaces.</span></span> <span data-ttu-id="1fa0b-113">O primeiro campo contém um valor de cadeia de caracteres que especifica o arquivo a ser executado.</span><span class="sxs-lookup"><span data-stu-id="1fa0b-113">The first field contains a string value that specifies the file that is to be run.</span></span> <span data-ttu-id="1fa0b-114">Use um valor de cadeia de caracteres de \[ \# *FileKey* \] para identificar o arquivo e substitua *FileKey* pelo identificador do arquivo que aparece na coluna arquivo da tabela de [arquivos](file-table.md) .</span><span class="sxs-lookup"><span data-stu-id="1fa0b-114">Use a string value of \[\#*filekey*\] to identify the file and replace *filekey* with the file's identifier appearing in the File column of the [File](file-table.md) table.</span></span> <span data-ttu-id="1fa0b-115">Todos os campos restantes do argumento podem conter parâmetros que estão sendo usados pelo arquivo que está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="1fa0b-115">Any remaining fields of the argument can contain parameters being used by the file being run.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="1fa0b-116">Ação nos assinantes</span><span class="sxs-lookup"><span data-stu-id="1fa0b-116">Action on Subscribers</span></span>

<span data-ttu-id="1fa0b-117">Este ControlEvent, não executa ações em assinantes.</span><span class="sxs-lookup"><span data-stu-id="1fa0b-117">This ControlEvent performs no actions on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="1fa0b-118">Usos comum</span><span class="sxs-lookup"><span data-stu-id="1fa0b-118">Typical Use</span></span>

<span data-ttu-id="1fa0b-119">Para permitir que um usuário escolha Executar um arquivo no final de uma instalação.</span><span class="sxs-lookup"><span data-stu-id="1fa0b-119">To enable a user to choose to run a file at the end of an installation.</span></span> <span data-ttu-id="1fa0b-120">Esse evento pode ser condicionado em uma propriedade definida por um controle de [caixa de seleção](checkbox-control.md) exibido na caixa de diálogo final da instalação.</span><span class="sxs-lookup"><span data-stu-id="1fa0b-120">This event can be conditioned on a property set by a [CheckBox](checkbox-control.md) control displayed on the final dialog box of the installation.</span></span> <span data-ttu-id="1fa0b-121">O controle de caixa de seleção não deve ser exibido durante a remoção do pacote.</span><span class="sxs-lookup"><span data-stu-id="1fa0b-121">The CheckBox control should not be displayed during the removal of the package.</span></span>

 

 



