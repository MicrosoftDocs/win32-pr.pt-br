---
description: A propriedade MSIARPSETTINGSIDENTIFIER contém uma lista delimitada por ponto e vírgula dos locais do registro onde o aplicativo armazena as configurações e preferências de um usuário.
ms.assetid: 524ba004-d3a2-4619-8c98-362761a3ae7a
title: Propriedade MSIARPSETTINGSIDENTIFIER
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a32c979237e6443bec5451f36e36ef49ae4a1f59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753440"
---
# <a name="msiarpsettingsidentifier-property"></a><span data-ttu-id="33528-103">Propriedade MSIARPSETTINGSIDENTIFIER</span><span class="sxs-lookup"><span data-stu-id="33528-103">MSIARPSETTINGSIDENTIFIER property</span></span>

<span data-ttu-id="33528-104">A propriedade **MSIARPSETTINGSIDENTIFIER** contém uma lista delimitada por ponto e vírgula dos locais do registro onde o aplicativo armazena as configurações e preferências de um usuário.</span><span class="sxs-lookup"><span data-stu-id="33528-104">The **MSIARPSETTINGSIDENTIFIER** property contains a semi-colon delimited list of the registry locations where the application stores a user's settings and preferences.</span></span> <span data-ttu-id="33528-105">Durante uma atualização do sistema operacional, a instalação pode usar essas informações para melhorar a experiência de usuários que estão migrando aplicativos.</span><span class="sxs-lookup"><span data-stu-id="33528-105">During an operating system upgrade, setup can use this information to improve the experience of users who are migrating applications.</span></span>

<span data-ttu-id="33528-106">O valor da propriedade **MSIARPSETTINGSIDENTIFIER** é um texto literal que contém a lista de locais de registro onde o aplicativo armazena suas configurações.</span><span class="sxs-lookup"><span data-stu-id="33528-106">The value of the **MSIARPSETTINGSIDENTIFIER** property is literal text that contains the list of registry locations where the application stores its settings.</span></span> <span data-ttu-id="33528-107">O valor pode especificar vários locais de registro possíveis.</span><span class="sxs-lookup"><span data-stu-id="33528-107">The value can specify multiple possible registry locations.</span></span> <span data-ttu-id="33528-108">Separe vários locais de registro usando ponto e vírgula.</span><span class="sxs-lookup"><span data-stu-id="33528-108">Separate multiple registry locations by using semi-colons.</span></span> <span data-ttu-id="33528-109">As configurações de aplicativo normalmente são armazenadas nos hives do registro **HKCU** ou **HKLM** no formato *: \\ \\ versão do aplicativo da empresa*.</span><span class="sxs-lookup"><span data-stu-id="33528-109">Application settings are typically stored in the **HKCU** or **HKLM** registry hives in the form: *Company\\Application\\Version*.</span></span> <span data-ttu-id="33528-110">O exemplo a seguir é um valor possível para a propriedade **MSIARPSETTINGSIDENTIFIER** .</span><span class="sxs-lookup"><span data-stu-id="33528-110">The following example is a possible value for the **MSIARPSETTINGSIDENTIFIER** property.</span></span>

<span data-ttu-id="33528-111">*MyCompany \\ AppSuite \\ 1,0; MyCompany \\ App1 \\ 1,0; MyCompany \\ App2 \\ 1,0*</span><span class="sxs-lookup"><span data-stu-id="33528-111">*MyCompany\\AppSuite\\1.0;MyCompany\\App1\\1.0;MyCompany\\App2\\1.0*</span></span>

<span data-ttu-id="33528-112">Essa propriedade é opcional e pode ser definida na tabela de [Propriedades](property-table.md) .</span><span class="sxs-lookup"><span data-stu-id="33528-112">This property is optional and can be set in the [Property](property-table.md) table.</span></span> <span data-ttu-id="33528-113">Se essa propriedade aparecer na tabela de propriedades, o valor não deverá ser definido como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="33528-113">If this property appears in the Property table, the value must not be set to **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="33528-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33528-114">Requirements</span></span>



| <span data-ttu-id="33528-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="33528-115">Requirement</span></span> | <span data-ttu-id="33528-116">Valor</span><span class="sxs-lookup"><span data-stu-id="33528-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33528-117">Versão</span><span class="sxs-lookup"><span data-stu-id="33528-117">Version</span></span><br/> | <span data-ttu-id="33528-118">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="33528-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="33528-119">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="33528-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="33528-120">Windows Installer 4,5 no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="33528-120">Windows Installer 4.5 on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="33528-121">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="33528-121">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="33528-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="33528-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33528-123">Propriedades</span><span class="sxs-lookup"><span data-stu-id="33528-123">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="33528-124">Sem suporte no Windows Installer 3,1 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="33528-124">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




