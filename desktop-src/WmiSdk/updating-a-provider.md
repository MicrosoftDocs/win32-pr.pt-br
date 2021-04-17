---
description: Às vezes, talvez seja necessário instalar uma versão mais recente de um provedor em um sistema em execução.
ms.assetid: 44c4c16a-fd79-483a-81ef-a0f74a2cdf45
ms.tgt_platform: multiple
title: Atualizando um provedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4869e6e9f7fbddc3081922f476ca021934065a18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105783763"
---
# <a name="updating-a-provider"></a><span data-ttu-id="7141e-103">Atualizando um provedor</span><span class="sxs-lookup"><span data-stu-id="7141e-103">Updating a Provider</span></span>

<span data-ttu-id="7141e-104">Às vezes, talvez seja necessário instalar uma versão mais recente de um provedor em um sistema em execução.</span><span class="sxs-lookup"><span data-stu-id="7141e-104">Sometimes you may need to install a newer version of a provider onto a running system.</span></span> <span data-ttu-id="7141e-105">Se seu provedor estiver instalado como uma DLL, você poderá instalar um novo provedor sem precisar reiniciar o serviço, reinicializar o computador ou, de outra forma, afetar os aplicativos que usam o WMI naquele momento.</span><span class="sxs-lookup"><span data-stu-id="7141e-105">If your provider is installed as a DLL, you can install a new provider without having to restart the service, reboot the computer, or otherwise affect any applications using WMI at that time.</span></span>

<span data-ttu-id="7141e-106">O procedimento a seguir descreve como atualizar um provedor.</span><span class="sxs-lookup"><span data-stu-id="7141e-106">The following procedure describes how to update a provider.</span></span>

<span data-ttu-id="7141e-107">**Para atualizar um provedor**</span><span class="sxs-lookup"><span data-stu-id="7141e-107">**To update a provider**</span></span>

1.  <span data-ttu-id="7141e-108">Crie o novo provedor.</span><span class="sxs-lookup"><span data-stu-id="7141e-108">Build the new provider.</span></span>

    1.  <span data-ttu-id="7141e-109">Compile o novo provedor com um nome de DLL diferente e um **CLSID** diferente.</span><span class="sxs-lookup"><span data-stu-id="7141e-109">Compile the new provider with a different DLL name and a different **CLSID**.</span></span>

        <span data-ttu-id="7141e-110">Por exemplo, altere Myprov.dll para Myprov1.dll e **CLSID \_ MyProProv** para **CLSID \_ MyProv** 1.</span><span class="sxs-lookup"><span data-stu-id="7141e-110">For example, change Myprov.dll to Myprov1.dll, and **CLSID\_MyProProv** to **CLSID\_MyProv** 1.</span></span>

    2.  <span data-ttu-id="7141e-111">Modifique o arquivo MOF de registro do provedor para usar o novo CLSID (CLSID \_ MyProv1), mas o mesmo nome do provedor ("MyProv").</span><span class="sxs-lookup"><span data-stu-id="7141e-111">Modify the provider registration MOF file to use the new CLSID (CLSID\_MyProv1), but the same provider name ("MyProv").</span></span>

2.  <span data-ttu-id="7141e-112">Instale o novo provedor.</span><span class="sxs-lookup"><span data-stu-id="7141e-112">Install the new provider.</span></span>

    1.  <span data-ttu-id="7141e-113">Copie a nova DLL do provedor com o novo nome junto com a antiga.</span><span class="sxs-lookup"><span data-stu-id="7141e-113">Copy the new provider DLL with the new name alongside the old one.</span></span>
    2.  <span data-ttu-id="7141e-114">Registrar automaticamente o novo provedor.</span><span class="sxs-lookup"><span data-stu-id="7141e-114">Self-register the new provider.</span></span>

        <span data-ttu-id="7141e-115">Por exemplo, use o comando **regsvr32** **myprov1.dll** para registrar o novo provedor.</span><span class="sxs-lookup"><span data-stu-id="7141e-115">For example, use the **regsvr32** **myprov1.dll** command to register the new provider.</span></span>

    3.  <span data-ttu-id="7141e-116">Compile o novo MOF de registro do provedor, substituindo assim o registro do provedor antigo.</span><span class="sxs-lookup"><span data-stu-id="7141e-116">Compile the new provider registration MOF, thus overwriting the old provider registration.</span></span> <span data-ttu-id="7141e-117">Até esse ponto, o antigo provedor era totalmente funcional; Agora o novo provedor está totalmente operacional.</span><span class="sxs-lookup"><span data-stu-id="7141e-117">Until this point, the old provider was fully functional; now the new provider is fully operational.</span></span>

3.  <span data-ttu-id="7141e-118">Remova a versão antiga do provedor, se necessário.</span><span class="sxs-lookup"><span data-stu-id="7141e-118">Remove the old version of the provider, if necessary.</span></span>

    1.  <span data-ttu-id="7141e-119">Cancele o registro da DLL antiga.</span><span class="sxs-lookup"><span data-stu-id="7141e-119">Unregister the old DLL.</span></span>

        <span data-ttu-id="7141e-120">Por exemplo, use o comando **regsvr32** **/umyprov.dll** para cancelar o registro da dll antiga.</span><span class="sxs-lookup"><span data-stu-id="7141e-120">For example, use the **regsvr32** **/umyprov.dll** command to unregister the old DLL.</span></span>

    2.  <span data-ttu-id="7141e-121">Marque a DLL antiga a ser excluída na reinicialização chamando [**MoveFileEx**](/windows/desktop/api/winbase/nf-winbase-movefileexa).</span><span class="sxs-lookup"><span data-stu-id="7141e-121">Mark the old DLL to be deleted on reboot by calling [**MoveFileEx**](/windows/desktop/api/winbase/nf-winbase-movefileexa).</span></span>

<span data-ttu-id="7141e-122">Você pode usar etapas semelhantes para atualizar um provedor implementado pelo servidor local.</span><span class="sxs-lookup"><span data-stu-id="7141e-122">You can take similar steps to upgrade a local server-implemented provider.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7141e-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7141e-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7141e-124">Desenvolvendo um provedor WMI</span><span class="sxs-lookup"><span data-stu-id="7141e-124">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md)
</dt> <dt>

[<span data-ttu-id="7141e-125">Configurando descritores de segurança namepace</span><span class="sxs-lookup"><span data-stu-id="7141e-125">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="7141e-126">Protegendo seu provedor</span><span class="sxs-lookup"><span data-stu-id="7141e-126">Securing Your Provider</span></span>](securing-your-provider.md)
</dt> </dl>

 

 
