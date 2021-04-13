---
description: Painel de controle do HKCU \\ \\ desktop.
ms.assetid: e18ea3c8-ddac-4214-83be-106c28c3c327
title: SCRNSAVE.EXE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77d6a5d50b002299fe38508b387926b0eed11141
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370470"
---
# <a name="scrnsaveexe"></a><span data-ttu-id="52cb1-103">SCRNSAVE.EXE</span><span class="sxs-lookup"><span data-stu-id="52cb1-103">SCRNSAVE.EXE</span></span>

<span data-ttu-id="52cb1-104">**Painel de controle do HKCU \\ \\ Desktop**</span><span class="sxs-lookup"><span data-stu-id="52cb1-104">**HKCU\\Control Panel\\Desktop**</span></span>



| <span data-ttu-id="52cb1-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="52cb1-105">Data type</span></span> | <span data-ttu-id="52cb1-106">Intervalo</span><span class="sxs-lookup"><span data-stu-id="52cb1-106">Range</span></span>       | <span data-ttu-id="52cb1-107">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="52cb1-107">Default value</span></span> |
|-----------|-------------|---------------|
| <span data-ttu-id="52cb1-108">REG \_ sz</span><span class="sxs-lookup"><span data-stu-id="52cb1-108">REG\_SZ</span></span>   | <span data-ttu-id="52cb1-109">*Nome do arquivo*</span><span class="sxs-lookup"><span data-stu-id="52cb1-109">*File name*</span></span> | <span data-ttu-id="52cb1-110">(Nenhuma)</span><span class="sxs-lookup"><span data-stu-id="52cb1-110">(None)</span></span>        |



 

## <a name="description"></a><span data-ttu-id="52cb1-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="52cb1-111">Description</span></span>

<span data-ttu-id="52cb1-112">Especifica o nome do arquivo executável de proteção de tela.</span><span class="sxs-lookup"><span data-stu-id="52cb1-112">Specifies the name of the screen saver executable file.</span></span>

## <a name="change-method"></a><span data-ttu-id="52cb1-113">Alterar Método</span><span class="sxs-lookup"><span data-stu-id="52cb1-113">Change Method</span></span>

<span data-ttu-id="52cb1-114">Para alterar o valor dessa entrada, no painel de controle, clique duas vezes em **Exibir**, clique na guia **proteção de tela** e selecione uma proteção de tela na lista **proteção de tela** .</span><span class="sxs-lookup"><span data-stu-id="52cb1-114">To change the value of this entry, in Control Panel double-click **Display**, click the **Screen Saver** tab, and then select a screen saver from the **Screen saver** list.</span></span>

<span data-ttu-id="52cb1-115">Você também pode alterar essa entrada com a função de API (interface de programação de aplicativo) **InstallScreenSaver**, que é exportada por Desk.cpl.</span><span class="sxs-lookup"><span data-stu-id="52cb1-115">You can also change this entry with the application programming interface (API) function **InstallScreenSaver**, which is exported by Desk.cpl.</span></span> <span data-ttu-id="52cb1-116">Você pode acessar essa função com a linha de comando **rundll32.exe desk.cpl,** o *arquivo* InstallScreenSaver, em que *File* é o nome de um arquivo executável de proteção de tela.</span><span class="sxs-lookup"><span data-stu-id="52cb1-116">You can access this function with the command line **rundll32.exe desk.cpl,InstallScreenSaver** *file*, where *file* is the name of a screen saver executable file.</span></span>

## <a name="activation-method"></a><span data-ttu-id="52cb1-117">Método de ativação</span><span class="sxs-lookup"><span data-stu-id="52cb1-117">Activation Method</span></span>

<span data-ttu-id="52cb1-118">As alterações feitas nessa entrada entram em vigor na próxima vez em que o sistema iniciar uma proteção de tela.</span><span class="sxs-lookup"><span data-stu-id="52cb1-118">Changes made to this entry become effective the next time the system starts a screen saver.</span></span> <span data-ttu-id="52cb1-119">As alterações feitas nessa entrada enquanto uma proteção de tela está em execução não têm efeito sobre a proteção de tela em execução.</span><span class="sxs-lookup"><span data-stu-id="52cb1-119">Changes made to this entry while a screen saver is running have no effect on the running screen saver.</span></span>

## <a name="notes"></a><span data-ttu-id="52cb1-120">Observações</span><span class="sxs-lookup"><span data-stu-id="52cb1-120">Notes</span></span>

-   <span data-ttu-id="52cb1-121">Os sistemas operacionais Windows adicionam essa entrada ao registro quando você usa **Exibir** no painel de controle para selecionar uma proteção de tela.</span><span class="sxs-lookup"><span data-stu-id="52cb1-121">Windows operating systems add this entry to the registry when you use **Display** in Control Panel to select a screen saver.</span></span> <span data-ttu-id="52cb1-122">Se você desabilitar todas as proteções de tela escolhendo **(nenhum)** na lista proteção de tela, o sistema operacional excluirá essa entrada do registro e chamará a função [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) com *uiAction* igual a SPI \_ SETSCREENSAVEACTIVE e *uiParam* igual a **false**.</span><span class="sxs-lookup"><span data-stu-id="52cb1-122">If you disable all screen savers by choosing **(None)** from the screen saver list, then the operating system deletes this entry from the registry and calls the [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function with *uiAction* equal to SPI\_SETSCREENSAVEACTIVE and *uiParam* equal to **FALSE**.</span></span>
-   <span data-ttu-id="52cb1-123">Essa entrada pode ser substituída por uma configuração de Política de Grupo em sistemas que dão suporte a Política de Grupo.</span><span class="sxs-lookup"><span data-stu-id="52cb1-123">This entry can be superseded by a Group Policy setting on systems that support Group Policy.</span></span> <span data-ttu-id="52cb1-124">Enquanto a configuração Política de Grupo **nome do executável de proteção de tela** está habilitada, o sistema ignora essa entrada.</span><span class="sxs-lookup"><span data-stu-id="52cb1-124">While the **Screen saver executable name** Group Policy setting is enabled, the system ignores this entry.</span></span> <span data-ttu-id="52cb1-125">A configuração dessa configuração de política é armazenada na entrada **SCRNSAVE.EXE** , que está na subchave **Policies** .</span><span class="sxs-lookup"><span data-stu-id="52cb1-125">The configuration of this policy setting is stored in the **SCRNSAVE.EXE** entry, which is in the **Policies** subkey.</span></span>

 

 
