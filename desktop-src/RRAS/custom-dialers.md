---
title: Discadores personalizados
description: Os sistemas operacionais Windows 2000 e posteriores permitem que os desenvolvedores forneçam seus próprios discadores personalizados que funcionam com o RAS (serviço de acesso remoto).
ms.assetid: ad94f38d-812f-4329-8055-6274a21a3242
keywords:
- Discadores personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35293de408a2a0faa146b93f9b5d5ebccf447acc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104162356"
---
# <a name="custom-dialers"></a><span data-ttu-id="e5164-104">Discadores personalizados</span><span class="sxs-lookup"><span data-stu-id="e5164-104">Custom Dialers</span></span>

<span data-ttu-id="e5164-105">Os sistemas operacionais Windows 2000 e posteriores permitem que os desenvolvedores forneçam seus próprios discadores personalizados que funcionam com o RAS (serviço de acesso remoto).</span><span class="sxs-lookup"><span data-stu-id="e5164-105">Windows 2000 and later operating systems enable developers to provide their own custom dialers that work with the Remote Access Service (RAS).</span></span> <span data-ttu-id="e5164-106">A discagem personalizada é implementada como uma única DLL (biblioteca de vínculo dinâmico) que exporta os seguintes pontos de entrada:</span><span class="sxs-lookup"><span data-stu-id="e5164-106">The custom dialer is implemented as a single dynamic-link library (DLL) that exports the following entry points:</span></span>

-   [<span data-ttu-id="e5164-107">**RasCustomDial**</span><span class="sxs-lookup"><span data-stu-id="e5164-107">**RasCustomDial**</span></span>](/windows/desktop/api/Ras/nc-ras-rascustomdialfn)
-   [<span data-ttu-id="e5164-108">**RasCustomDialDlg**</span><span class="sxs-lookup"><span data-stu-id="e5164-108">**RasCustomDialDlg**</span></span>](/windows/desktop/api/Rasdlg/nc-rasdlg-rascustomdialdlgfn)
-   [<span data-ttu-id="e5164-109">**RasCustomHangup**</span><span class="sxs-lookup"><span data-stu-id="e5164-109">**RasCustomHangup**</span></span>](/windows/desktop/api/Ras/nc-ras-rascustomhangupfn)
-   [<span data-ttu-id="e5164-110">**RasCustomEntryDlg**</span><span class="sxs-lookup"><span data-stu-id="e5164-110">**RasCustomEntryDlg**</span></span>](/windows/desktop/api/Rasdlg/nc-rasdlg-rascustomentrydlgfn)
-   [<span data-ttu-id="e5164-111">**RasCustomDeleteEntryNotify**</span><span class="sxs-lookup"><span data-stu-id="e5164-111">**RasCustomDeleteEntryNotify**</span></span>](/windows/desktop/api/Ras/nc-ras-rascustomdeleteentrynotifyfn)

<span data-ttu-id="e5164-112">A DLL de discagem personalizada deve exportar todos esses pontos de entrada e deve implementar os pontos de entrada como funções Unicode.</span><span class="sxs-lookup"><span data-stu-id="e5164-112">The custom-dial DLL must export all of these entry points, and it must implement the entry points as Unicode functions.</span></span> <span data-ttu-id="e5164-113">Para obter mais informações sobre essas funções, consulte a página de referência de cada função na referência do serviço de acesso remoto SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="e5164-113">For more information about these functions, see the reference page for each function in the Windows SDK Remote Access Service Reference.</span></span>

<span data-ttu-id="e5164-114">Para que uma conexão RAS use a discagem personalizada, a entrada do catálogo telefônico para a conexão deve conter o caminho para a DLL de discagem personalizada.</span><span class="sxs-lookup"><span data-stu-id="e5164-114">In order for a RAS connection to use the custom dialer, the phone-book entry for the connection must contain the path to the custom-dial DLL.</span></span> <span data-ttu-id="e5164-115">Use as funções de API RAS [**RasGetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rasgetentrypropertiesa) e [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) para definir esse caminho no membro **szCustomDialDll** da estrutura [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) para a entrada de catálogo telefônico.</span><span class="sxs-lookup"><span data-stu-id="e5164-115">Use the RAS API functions [**RasGetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rasgetentrypropertiesa) and [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) to set this path in the **szCustomDialDll** member of the [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) structure for the phone-book entry.</span></span>

## <a name="updating-the-registry-for-custom-dialers"></a><span data-ttu-id="e5164-116">Atualizando o registro para discadores personalizados</span><span class="sxs-lookup"><span data-stu-id="e5164-116">Updating the Registry for Custom Dialers</span></span>

<span data-ttu-id="e5164-117">Para que o sistema disque uma conexão que usa uma discagem personalizada, o caminho para a DLL de discagem personalizada deve existir no valor do registro a seguir.</span><span class="sxs-lookup"><span data-stu-id="e5164-117">In order for the system to dial a connection that uses a custom dialer, the path to the custom-dial DLL must exist in the following registry value.</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Rasman
               Parameters
                  CustomDLL<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_MULTI_SZ</dd>
</dl>
```

<span data-ttu-id="e5164-118">Como **CustomDLL** é do tipo **reg \_ multi \_ sz**, ele pode conter caminhos para várias DLLs de discagem personalizada.</span><span class="sxs-lookup"><span data-stu-id="e5164-118">Because **CustomDLL** is of type **REG\_MULTI\_SZ**, it can hold paths to multiple custom-dial DLLs.</span></span> <span data-ttu-id="e5164-119">Você precisa definir o caminho para a DLL de discagem personalizada nesse valor de registro, além da entrada de catálogo telefônico para a conexão.</span><span class="sxs-lookup"><span data-stu-id="e5164-119">You need to set the path to the custom-dial DLL in this registry value, in addition to the phone-book entry for the connection.</span></span>

<span data-ttu-id="e5164-120">Por padrão, esse valor de registro é gravável somente por um usuário com privilégios de administrador ou de sistema.</span><span class="sxs-lookup"><span data-stu-id="e5164-120">By default, this registry value is writeable only by a user with Administrator or System privileges.</span></span> <span data-ttu-id="e5164-121">Por motivos de segurança, não altere as permissões nessa chave do registro.</span><span class="sxs-lookup"><span data-stu-id="e5164-121">For security reasons, do not change the permissions on this registry key.</span></span>

## <a name="using-custom-dialers-at-system-logon"></a><span data-ttu-id="e5164-122">Usando discadores personalizados no logon do sistema</span><span class="sxs-lookup"><span data-stu-id="e5164-122">Using Custom Dialers at System Logon</span></span>

<span data-ttu-id="e5164-123">Os sistemas operacionais Windows 2000 e posteriores permitem que um usuário estabeleça uma conexão RAS no momento do logon.</span><span class="sxs-lookup"><span data-stu-id="e5164-123">Windows 2000 and later operating systems allow a user to establish a RAS connection at the time of logon.</span></span> <span data-ttu-id="e5164-124">Para fazer isso, o usuário verifica o **logon usando a rede dial-up** na caixa de diálogo **informações de logon** .</span><span class="sxs-lookup"><span data-stu-id="e5164-124">To do so, the user checks **Logon using Dial-up Networking** in the **Logon Information** dialog box.</span></span> <span data-ttu-id="e5164-125">Depois que o usuário clicar no botão OK, o sistema exibirá as conexões disponíveis.</span><span class="sxs-lookup"><span data-stu-id="e5164-125">After the user clicks the Okay button, the system displays the available connections.</span></span>

## <a name="security-considerations"></a><span data-ttu-id="e5164-126">Considerações de segurança</span><span class="sxs-lookup"><span data-stu-id="e5164-126">Security Considerations</span></span>

<span data-ttu-id="e5164-127">Na maioria dos casos, uma discagem personalizada opera com os privilégios de segurança do usuário que a invoca.</span><span class="sxs-lookup"><span data-stu-id="e5164-127">In most cases, a custom dialer operates with the security privileges of the user that invokes it.</span></span> <span data-ttu-id="e5164-128">No entanto, se a discagem personalizada for invocada no logon, ela funcionará com privilégios de sistema.</span><span class="sxs-lookup"><span data-stu-id="e5164-128">However, if the custom dialer is invoked at logon, it operates with system privileges.</span></span> <span data-ttu-id="e5164-129">Portanto, projete a discagem personalizada para que ela não possa ser usada para violar a segurança do sistema.</span><span class="sxs-lookup"><span data-stu-id="e5164-129">Therefore, design the custom dialer so that it cannot be used to violate system security.</span></span> <span data-ttu-id="e5164-130">Por exemplo, a discagem não deve apresentar uma interface do usuário que permita ao usuário gravar o acesso ao sistema de arquivos do computador.</span><span class="sxs-lookup"><span data-stu-id="e5164-130">For example, the dialer should not present a user interface that allows the user write access to the computer's file system.</span></span> <span data-ttu-id="e5164-131">As interfaces do usuário que fornecem esse acesso incluem a caixa de diálogo **Find-File** , a caixa de diálogo comum **Abrir arquivo** e a **ajuda** do Windows.</span><span class="sxs-lookup"><span data-stu-id="e5164-131">User interfaces that provide such access include the **Find-File** dialog, the **File-Open** common dialog, and Windows **Help**.</span></span>

## <a name="custom-dialer-user-interface-must-support-idcancel"></a><span data-ttu-id="e5164-132">A interface do usuário do discador personalizado deve dar suporte a IDCANCEL</span><span class="sxs-lookup"><span data-stu-id="e5164-132">Custom Dialer User Interface Must Support IDCANCEL</span></span>

<span data-ttu-id="e5164-133">Se a discagem personalizada exibir uma interface do usuário, a interface do usuário deverá dar suporte a \_ mensagens de comando do WM em que LOWORD (*wParam*) seja igual a IDCANCEL.</span><span class="sxs-lookup"><span data-stu-id="e5164-133">If the custom dialer displays a user interface, the user interface must support WM\_COMMAND messages where LOWORD(*wParam*) equals IDCANCEL.</span></span>

 

 