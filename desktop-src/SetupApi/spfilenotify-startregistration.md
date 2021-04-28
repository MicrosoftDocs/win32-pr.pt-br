---
description: SPFILENOTIFY_STARTREGISTRATION mensagem-ao usar a diretiva RegisterDlls INF para autoregistrar DLLs, os chamadores de SetupInstallFromInfSection podem receber notificações em cada arquivo, já que são registrados ou cancelados.
ms.assetid: 0faf277c-7805-478f-9cec-0dd7b6acdb0e
title: Mensagem de SPFILENOTIFY_STARTREGISTRATION (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47e71a884d079515436f296faf515a83a985311e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094494"
---
# <a name="spfilenotify_startregistration-message"></a><span data-ttu-id="58ace-103">\_Mensagem SPFILENOTIFY STARTREGISTRATION</span><span class="sxs-lookup"><span data-stu-id="58ace-103">SPFILENOTIFY\_STARTREGISTRATION message</span></span>

<span data-ttu-id="58ace-104">Ao usar a diretiva **RegisterDlls** inf para Autoregistro de DLLs, os chamadores de [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) podem receber notificações em cada arquivo conforme ele é registrado ou cancelado.</span><span class="sxs-lookup"><span data-stu-id="58ace-104">When using the **RegisterDlls** INF directive to self-register DLLs, callers of [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) may receive notifications on each file as it is registered or unregistered.</span></span> <span data-ttu-id="58ace-105">Para enviar uma notificação **SPFILENOTIFY \_ STARTREGISTRATION** para a rotina de retorno de chamada uma vez antes de registrar um arquivo, inclua \_ o REGISTERCALLBACKAWARE mais giratório e \_ o regsvr mais giratório no parâmetro *flags* de **SetupInstallFromInfSection**.</span><span class="sxs-lookup"><span data-stu-id="58ace-105">To send a **SPFILENOTIFY\_STARTREGISTRATION** notification to the callback routine once before registering a file, include SPINST\_REGISTERCALLBACKAWARE plus SPINST\_REGSVR in the *Flags* parameter of **SetupInstallFromInfSection**.</span></span> <span data-ttu-id="58ace-106">Para enviar a notificação de cancelamento de registro, inclua \_ o REGISTERCALLBACKAWARE mais giratório e o UNREGSVR mais giratório \_ no parâmetro *flags* .</span><span class="sxs-lookup"><span data-stu-id="58ace-106">To send notification of unregistration, include SPINST\_REGISTERCALLBACKAWARE plus SPINST\_UNREGSVR in the *Flags* parameter.</span></span>

<span data-ttu-id="58ace-107">A rotina de retorno de chamada especificada pelo parâmetro *MsgHandler* de [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) deve ser o tipo de [retorno de \_ \_ chamada de arquivo PSP](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a).</span><span class="sxs-lookup"><span data-stu-id="58ace-107">The callback routine specified by the *MsgHandler* parameter of [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) must be the type [PSP\_FILE\_CALLBACK](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a).</span></span> <span data-ttu-id="58ace-108">Defina o parâmetro de *contexto* para o mesmo *contexto* especificado em **SetupInstallFromInfSection**.</span><span class="sxs-lookup"><span data-stu-id="58ace-108">Set the *Context* parameter to the same *Context* specified in **SetupInstallFromInfSection**.</span></span> <span data-ttu-id="58ace-109">Defina o parâmetro de *notificação* como **SPFILENOTIFY \_ STARTREGISTRATION**.</span><span class="sxs-lookup"><span data-stu-id="58ace-109">Set the *Notification* parameter to **SPFILENOTIFY\_STARTREGISTRATION**.</span></span>


```C++
SPFILENOTIFY_STARTREGISTRATION
  Param1 = (UINT_PTR) pointer to file information;
  Param2 = (UINT_PTR) file registration or unregistration;
            
```



## <a name="parameters"></a><span data-ttu-id="58ace-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="58ace-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58ace-111">*Param1*</span><span class="sxs-lookup"><span data-stu-id="58ace-111">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="58ace-112">Ponteiro para uma estrutura de status de controle de registro do SP que contém informações sobre o arquivo que está sendo registrado ou não registrado. [**\_ \_ \_**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa)</span><span class="sxs-lookup"><span data-stu-id="58ace-112">Pointer to a [**SP\_REGISTER\_CONTROL\_STATUS**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa) structure containing information about the file being registered or unregistered.</span></span> <span data-ttu-id="58ace-113">O membro **cbSize** deve ser definido como o tamanho da estrutura.</span><span class="sxs-lookup"><span data-stu-id="58ace-113">The member **cbsize** should be set to the size of the structure.</span></span> <span data-ttu-id="58ace-114">O membro **filename** deve ser definido como o caminho totalmente qualificado do arquivo que está sendo registrado.</span><span class="sxs-lookup"><span data-stu-id="58ace-114">The **FileName** member should be set to the fully qualified path of the file being registered.</span></span> <span data-ttu-id="58ace-115">**Win32Error** não é usado e deve ser definido como sem \_ erro.</span><span class="sxs-lookup"><span data-stu-id="58ace-115">**Win32Error** is not used and should be set to NO\_ERROR.</span></span> <span data-ttu-id="58ace-116">**FailureCode** não é usado e deve ser definido como SPREG \_ Success.</span><span class="sxs-lookup"><span data-stu-id="58ace-116">**FailureCode** is not used and should be set to SPREG\_SUCCESS.</span></span>

</dd> <dt>

<span data-ttu-id="58ace-117">*Param2*</span><span class="sxs-lookup"><span data-stu-id="58ace-117">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="58ace-118">Se o arquivo estiver sendo registrado, *param2* deverá ser definido como um ponteiro para um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="58ace-118">If the file is being registered, *Param2* should be set to a pointer to a nonzero value.</span></span> <span data-ttu-id="58ace-119">Se o registro do arquivo estiver sendo cancelado, *param2* deverá ser definido como um ponteiro para zero.</span><span class="sxs-lookup"><span data-stu-id="58ace-119">If the file is being unregistered, *Param2* should be set to a pointer to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58ace-120">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="58ace-120">Return value</span></span>

<span data-ttu-id="58ace-121">Depois de receber a notificação, a função de retorno de chamada pode retornar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="58ace-121">After receiving notification, the callback function may return one of the following values.</span></span>



| <span data-ttu-id="58ace-122">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="58ace-122">Return code</span></span>                                                                                  | <span data-ttu-id="58ace-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="58ace-123">Description</span></span>                                                                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="58ace-124"><dt>**\_anular FILEOP**</dt></span><span class="sxs-lookup"><span data-stu-id="58ace-124"><dt>**FILEOP\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="58ace-125">Não registre ou cancele o registro do arquivo e pare de processar a seção INF.</span><span class="sxs-lookup"><span data-stu-id="58ace-125">Do not register or unregister the file and stop processing the INF section.</span></span><br/>             |
| <dl> <span data-ttu-id="58ace-126"><dt>**FILEOP \_ doit**</dt></span><span class="sxs-lookup"><span data-stu-id="58ace-126"><dt>**FILEOP\_DOIT**</dt></span></span> </dl>  | <span data-ttu-id="58ace-127">Registre ou cancele o registro do arquivo e continue processando a seção INF.</span><span class="sxs-lookup"><span data-stu-id="58ace-127">Register or unregister the file and continue processing the INF section.</span></span><br/>                |
| <dl> <span data-ttu-id="58ace-128"><dt>**\_ignorar arquivo**</dt></span><span class="sxs-lookup"><span data-stu-id="58ace-128"><dt>**FILE\_SKIP**</dt></span></span> </dl>    | <span data-ttu-id="58ace-129">Ignorar registro ou cancelamento de registro do arquivo, mas continuar processando a seção INF</span><span class="sxs-lookup"><span data-stu-id="58ace-129">Skip registration or unregistration of the file but continue processing the INF section</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="58ace-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58ace-130">Requirements</span></span>



| <span data-ttu-id="58ace-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="58ace-131">Requirement</span></span> | <span data-ttu-id="58ace-132">Valor</span><span class="sxs-lookup"><span data-stu-id="58ace-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="58ace-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="58ace-133">Minimum supported client</span></span><br/> | <span data-ttu-id="58ace-134">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="58ace-134">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="58ace-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="58ace-135">Minimum supported server</span></span><br/> | <span data-ttu-id="58ace-136">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="58ace-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="58ace-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="58ace-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="58ace-138"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="58ace-138"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58ace-139">Consulte também</span><span class="sxs-lookup"><span data-stu-id="58ace-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58ace-140">Visão geral</span><span class="sxs-lookup"><span data-stu-id="58ace-140">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="58ace-141">Notificações</span><span class="sxs-lookup"><span data-stu-id="58ace-141">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="58ace-142">**SetupInstallFromInfSection**</span><span class="sxs-lookup"><span data-stu-id="58ace-142">**SetupInstallFromInfSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> <dt>

[<span data-ttu-id="58ace-143">**SPFILENOTIFY \_ ENDregistro**</span><span class="sxs-lookup"><span data-stu-id="58ace-143">**SPFILENOTIFY\_ENDREGISTRATION**</span></span>](spfilenotify-endregistration.md)
</dt> </dl>

 

