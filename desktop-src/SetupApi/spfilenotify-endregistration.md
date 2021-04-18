---
description: Ao usar a diretiva RegisterDlls INF para Autoregistro de DLLs, os chamadores de SetupInstallFromInfSection podem receber notificações em cada arquivo conforme ele é registrado ou cancelado.
ms.assetid: 6304f406-c9f8-41cc-a7b7-5ef606f62efb
title: Mensagem de SPFILENOTIFY_ENDREGISTRATION (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c8992d318d605110d74521efdb8a9c911aeeb9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756362"
---
# <a name="spfilenotify_endregistration-message"></a><span data-ttu-id="6312f-103">\_Mensagem de ENDregistro do SPFILENOTIFY</span><span class="sxs-lookup"><span data-stu-id="6312f-103">SPFILENOTIFY\_ENDREGISTRATION message</span></span>

<span data-ttu-id="6312f-104">Ao usar a diretiva **RegisterDlls** inf para Autoregistro de DLLs, os chamadores de [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) podem receber notificações em cada arquivo conforme ele é registrado ou cancelado.</span><span class="sxs-lookup"><span data-stu-id="6312f-104">When using the **RegisterDlls** INF directive to self-register DLLs, callers of [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) may receive notifications on each file as it is registered or unregistered.</span></span> <span data-ttu-id="6312f-105">Para enviar uma notificação de **\_ endregistro do SPFILENOTIFY** para uma rotina de retorno de chamada uma vez depois de registrar ou cancelar o registro de um arquivo, inclua \_ o REGISTERCALLBACKAWARE mais giratório do \_ regsvr no parâmetro *flags* de **SetupInstallFromInfSection**.</span><span class="sxs-lookup"><span data-stu-id="6312f-105">To send a **SPFILENOTIFY\_ENDREGISTRATION** notification to a callback routine once after registering or unregistering a file, include SPINST\_REGISTERCALLBACKAWARE plus SPINST\_REGSVR in the *Flags* parameter of **SetupInstallFromInfSection**.</span></span> <span data-ttu-id="6312f-106">Para enviar a notificação de cancelamento de registro, inclua \_ o REGISTERCALLBACKAWARE mais giratório e o UNREGSVR mais giratório \_ no parâmetro *flags* .</span><span class="sxs-lookup"><span data-stu-id="6312f-106">To send notification of unregistration, include SPINST\_REGISTERCALLBACKAWARE plus SPINST\_UNREGSVR in the *Flags* parameter.</span></span>

<span data-ttu-id="6312f-107">A rotina de retorno de chamada especificada pelo parâmetro *MsgHandler* de [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) deve ser o tipo de [retorno de \_ \_ chamada de arquivo PSP](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a).</span><span class="sxs-lookup"><span data-stu-id="6312f-107">The callback routine specified by the *MsgHandler* parameter of [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) must be the type [PSP\_FILE\_CALLBACK](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a).</span></span> <span data-ttu-id="6312f-108">Defina o parâmetro de *contexto* para o mesmo *contexto* especificado em **SetupInstallFromInfSection**.</span><span class="sxs-lookup"><span data-stu-id="6312f-108">Set the *Context* parameter to the same *Context* specified in **SetupInstallFromInfSection**.</span></span> <span data-ttu-id="6312f-109">Defina o parâmetro de *notificação* como **SPFILENOTIFY \_ endregistro**.</span><span class="sxs-lookup"><span data-stu-id="6312f-109">Set the *Notification* parameter to **SPFILENOTIFY\_ENDREGISTRATION**.</span></span>


```C++
SPFILENOTIFY_ENDREGISTRATION
  Param1 = (UINT_PTR) pointer to file information;
  Param2 = (UINT_PTR) file registration or unregistration;
            
```



## <a name="parameters"></a><span data-ttu-id="6312f-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6312f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6312f-111">*Param1*</span><span class="sxs-lookup"><span data-stu-id="6312f-111">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="6312f-112">Ponteiro para uma estrutura de status de controle de registro do SP que contém informações sobre o arquivo que está sendo registrado ou não registrado. [**\_ \_ \_**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa)</span><span class="sxs-lookup"><span data-stu-id="6312f-112">Pointer to a [**SP\_REGISTER\_CONTROL\_STATUS**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa) structure containing information about the file being registered or unregistered.</span></span> <span data-ttu-id="6312f-113">O membro **cbSize** deve ser definido como o tamanho da estrutura.</span><span class="sxs-lookup"><span data-stu-id="6312f-113">The member **cbsize** should be set to the size of the structure.</span></span> <span data-ttu-id="6312f-114">**Filename** deve ser definido como o caminho totalmente qualificado do arquivo que está sendo registrado.</span><span class="sxs-lookup"><span data-stu-id="6312f-114">**FileName** should be set to the fully qualified path of the file being registered.</span></span> <span data-ttu-id="6312f-115">**Win32Error** deve ser definido como um [código de erro do sistema](/windows/desktop/Debug/system-error-codes) indicando um código de erro estendido.</span><span class="sxs-lookup"><span data-stu-id="6312f-115">**Win32Error** should be set to a [system error code](/windows/desktop/Debug/system-error-codes) indicating an extended error code.</span></span> <span data-ttu-id="6312f-116">**FailureCode** deve ser definido como um dos códigos de falha válidos indicando o resultado do registro.</span><span class="sxs-lookup"><span data-stu-id="6312f-116">**FailureCode** should be set to one of the valid failure codes indicating the outcome of the registration.</span></span> <span data-ttu-id="6312f-117">Para obter códigos de falha válidos, consulte [**status do controle de registro do SP \_ \_ \_**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa).</span><span class="sxs-lookup"><span data-stu-id="6312f-117">For valid failure codes see [**SP\_REGISTER\_CONTROL\_STATUS**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa).</span></span>

</dd> <dt>

<span data-ttu-id="6312f-118">*Param2*</span><span class="sxs-lookup"><span data-stu-id="6312f-118">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="6312f-119">Se o arquivo estiver sendo registrado, *param2* deverá ser definido como um ponteiro para um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="6312f-119">If the file is being registered, *Param2* should be set to a pointer to a nonzero value.</span></span> <span data-ttu-id="6312f-120">Se o registro do arquivo estiver sendo cancelado, *param2* deverá ser definido como um ponteiro para zero.</span><span class="sxs-lookup"><span data-stu-id="6312f-120">If the file is being unregistered, *Param2* should be set to a pointer to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6312f-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6312f-121">Return value</span></span>

<span data-ttu-id="6312f-122">Depois de receber a notificação, a função de retorno de chamada pode retornar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="6312f-122">After receiving notification, the callback function may return one of the following values.</span></span>



| <span data-ttu-id="6312f-123">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="6312f-123">Return code</span></span>                                                                                  | <span data-ttu-id="6312f-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="6312f-124">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="6312f-125"><dt>**\_anular FILEOP**</dt></span><span class="sxs-lookup"><span data-stu-id="6312f-125"><dt>**FILEOP\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="6312f-126">Pare de processar a seção INF.</span><span class="sxs-lookup"><span data-stu-id="6312f-126">Stop processing the INF section.</span></span><br/>     |
| <dl> <span data-ttu-id="6312f-127"><dt>**FILEOP \_ doit**</dt></span><span class="sxs-lookup"><span data-stu-id="6312f-127"><dt>**FILEOP\_DOIT**</dt></span></span> </dl>  | <span data-ttu-id="6312f-128">Continue processando a seção INF.</span><span class="sxs-lookup"><span data-stu-id="6312f-128">Continue processing the INF section.</span></span><br/> |
| <dl> <span data-ttu-id="6312f-129"><dt>**\_ignorar arquivo**</dt></span><span class="sxs-lookup"><span data-stu-id="6312f-129"><dt>**FILE\_SKIP**</dt></span></span> </dl>    | <span data-ttu-id="6312f-130">Continuar processando a seção INF</span><span class="sxs-lookup"><span data-stu-id="6312f-130">Continue processing the INF section</span></span><br/>  |



 

## <a name="requirements"></a><span data-ttu-id="6312f-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6312f-131">Requirements</span></span>



| <span data-ttu-id="6312f-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="6312f-132">Requirement</span></span> | <span data-ttu-id="6312f-133">Valor</span><span class="sxs-lookup"><span data-stu-id="6312f-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6312f-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6312f-134">Minimum supported client</span></span><br/> | <span data-ttu-id="6312f-135">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6312f-135">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="6312f-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6312f-136">Minimum supported server</span></span><br/> | <span data-ttu-id="6312f-137">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6312f-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6312f-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6312f-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="6312f-139"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="6312f-139"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6312f-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="6312f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6312f-141">Visão geral</span><span class="sxs-lookup"><span data-stu-id="6312f-141">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="6312f-142">Notificações</span><span class="sxs-lookup"><span data-stu-id="6312f-142">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="6312f-143">**SetupInstallFromInfSection**</span><span class="sxs-lookup"><span data-stu-id="6312f-143">**SetupInstallFromInfSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> <dt>

[<span data-ttu-id="6312f-144">**SPFILENOTIFY \_ STARTREGISTRATION**</span><span class="sxs-lookup"><span data-stu-id="6312f-144">**SPFILENOTIFY\_STARTREGISTRATION**</span></span>](spfilenotify-startregistration.md)
</dt> </dl>

 

