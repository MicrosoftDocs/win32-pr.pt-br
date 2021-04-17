---
description: Se ocorrer um erro, o WMI retornará um código de erro como um valor HRESULT. Esses códigos podem ser retornados por scripts, aplicativos C++ ou WMIC.
ms.assetid: b560f37c-da22-4745-8d1f-b27afdf572ec
ms.tgt_platform: multiple
title: Constantes de erro de WMI (WbemCli. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e95db7220bdc9669716dbe19f5bf2f4e139dfe5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105791441"
---
# <a name="wmi-error-constants"></a><span data-ttu-id="41d1d-104">Constantes de erro WMI</span><span class="sxs-lookup"><span data-stu-id="41d1d-104">WMI Error Constants</span></span>

<span data-ttu-id="41d1d-105">Se ocorrer um erro, o WMI retornará um código de erro como um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="41d1d-105">If an error occurs, WMI returns an error code as an **HRESULT** value.</span></span> <span data-ttu-id="41d1d-106">Esses códigos podem ser retornados por scripts, aplicativos C++ ou [**WMIC**](wmic.md).</span><span class="sxs-lookup"><span data-stu-id="41d1d-106">These codes may be returned by scripts, C++ applications, or [**Wmic**](wmic.md).</span></span>

> [!Note]
>
> <span data-ttu-id="41d1d-107">A documentação a seguir destina-se a desenvolvedores e administradores de ti.</span><span class="sxs-lookup"><span data-stu-id="41d1d-107">The following documentation is targeted for developers and IT administrators.</span></span> <span data-ttu-id="41d1d-108">Se você for um usuário final que recebeu uma mensagem de erro relacionada ao WMI, vá para [suporte da Microsoft](https://support.microsoft.com/) e procure o código de erro que você vê na mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="41d1d-108">If you are an end-user that has experienced an error message concerning WMI, you should go to [Microsoft Support](https://support.microsoft.com/) and search for the error code you see on the error message.</span></span> <span data-ttu-id="41d1d-109">Para obter mais informações sobre como solucionar problemas com scripts WMI e o serviço WMI, consulte o [WMI não está funcionando!](/previous-versions/tn-archive/ff406382(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="41d1d-109">For more information about troubleshooting problems with WMI scripts and the WMI service, see [WMI Isn't Working!](/previous-versions/tn-archive/ff406382(v=msdn.10)).</span></span>
>
> <span data-ttu-id="41d1d-110">Se o WMI retornar mensagens de erro, lembre-se de que eles podem não indicar problemas no serviço WMI ou em provedores WMI.</span><span class="sxs-lookup"><span data-stu-id="41d1d-110">If WMI returns error messages, be aware that they may not indicate problems in the WMI service or in WMI providers.</span></span> <span data-ttu-id="41d1d-111">As falhas podem se originar em outras partes do sistema operacional e surgir como erros por meio do WMI.</span><span class="sxs-lookup"><span data-stu-id="41d1d-111">Failures can originate in other parts of the operating system and emerge as errors through WMI.</span></span> <span data-ttu-id="41d1d-112">Em qualquer circunstância, não exclua o repositório WMI como uma primeira ação, pois a exclusão do repositório pode causar danos ao sistema ou aos aplicativos instalados.</span><span class="sxs-lookup"><span data-stu-id="41d1d-112">Under any circumstances, do not delete the WMI repository as a first action because deleting the repository can cause damage to the system or to installed applications.</span></span>
>
> <span data-ttu-id="41d1d-113">Para obter mais informações sobre a origem do problema, você pode baixar e executar a ferramenta de linha de comando de diagnóstico [Utilitário de diagnóstico WMI](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) .</span><span class="sxs-lookup"><span data-stu-id="41d1d-113">To obtain more information about the source of the problem, you can download and run the [WMI Diagnosis Utility](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) diagnostic command line tool.</span></span> <span data-ttu-id="41d1d-114">Essa ferramenta produz um relatório que, em geral, pode isolar a origem do problema e fornecer instruções sobre como corrigi-lo.</span><span class="sxs-lookup"><span data-stu-id="41d1d-114">This tool produces a report that can usually isolate the source of the problem and provide instructions on how to fix it.</span></span> <span data-ttu-id="41d1d-115">O relatório também ajuda os serviços de suporte da Microsoft para ajudá-lo.</span><span class="sxs-lookup"><span data-stu-id="41d1d-115">The report also aids Microsoft support services in assisting you.</span></span> <span data-ttu-id="41d1d-116">Você pode baixar o Utilitário de Diagnóstico WMI [aqui](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d).</span><span class="sxs-lookup"><span data-stu-id="41d1d-116">You can download the WMI Diagnosis Utility [here](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d).</span></span>

 

<span data-ttu-id="41d1d-117">Alguns métodos em classes WMI podem retornar códigos de erro de sistema e rede (64, por exemplo).</span><span class="sxs-lookup"><span data-stu-id="41d1d-117">Some methods in WMI classes can return system and network error codes (64 for example).</span></span> <span data-ttu-id="41d1d-118">Você pode verificar a definição desses tipos de códigos de erro usando o comando **net helpmsg** na janela do prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="41d1d-118">You can check the definition of these types of error codes by using the **net helpmsg** command in the command prompt window.</span></span> <span data-ttu-id="41d1d-119">Por exemplo, o comando **net helpmsg 64** retorna a mensagem: o nome de rede especificado não está mais disponível.</span><span class="sxs-lookup"><span data-stu-id="41d1d-119">For example, the command **net helpmsg 64** returns the message: The specified network name is no longer available.</span></span>

<span data-ttu-id="41d1d-120">A lista a seguir lista alguns intervalos de erros comuns.</span><span class="sxs-lookup"><span data-stu-id="41d1d-120">The following list lists some common ranges of errors.</span></span>

<dl> <dt>

<span data-ttu-id="41d1d-121"><span id="0x80041068_-_0x80041099"></span><span id="0X80041068_-_0X80041099"></span>0x80041068 - 0x80041099</span><span class="sxs-lookup"><span data-stu-id="41d1d-121"><span id="0x80041068_-_0x80041099"></span><span id="0X80041068_-_0X80041099"></span>0x80041068 - 0x80041099</span></span>
</dt> <dd>

<span data-ttu-id="41d1d-122">Erros originados no próprio WMI.</span><span class="sxs-lookup"><span data-stu-id="41d1d-122">Errors that originate in WMI itself.</span></span>

<span data-ttu-id="41d1d-123">Uma operação WMI específica falhou devido a</span><span class="sxs-lookup"><span data-stu-id="41d1d-123">A specific WMI operation failed because of</span></span>

-   <span data-ttu-id="41d1d-124">Um erro na solicitação, por exemplo, uma consulta WQL falha ou a conta não tem as permissões corretas.</span><span class="sxs-lookup"><span data-stu-id="41d1d-124">An error in the request, for example, a WQL query fails or the account does not have the correct permissions.</span></span>
-   <span data-ttu-id="41d1d-125">Um problema de infraestrutura do WMI, como registro incorreto de CIM ou DCOM.</span><span class="sxs-lookup"><span data-stu-id="41d1d-125">A WMI infrastructure problem, such as incorrect CIM or DCOM registration.</span></span>

</dd> <dt>

<span data-ttu-id="41d1d-126"><span id="0x8007xxxx"></span><span id="0X8007XXXX"></span>0x8007xxxx</span><span class="sxs-lookup"><span data-stu-id="41d1d-126"><span id="0x8007xxxx"></span><span id="0X8007XXXX"></span>0x8007xxxx</span></span>
</dt> <dd>

<span data-ttu-id="41d1d-127">Erros originados no sistema operacional principal.</span><span class="sxs-lookup"><span data-stu-id="41d1d-127">Errors originating in the core operating system.</span></span> <span data-ttu-id="41d1d-128">O WMI pode retornar esse tipo de erro devido a uma falha externa, por exemplo, falha de segurança DCOM.</span><span class="sxs-lookup"><span data-stu-id="41d1d-128">WMI may return this type of error because of an external failure, for example, DCOM security failure.</span></span>

</dd> <dt>

<span data-ttu-id="41d1d-129"><span id="0x80040xxx"></span><span id="0X80040XXX"></span>0x80040xxx</span><span class="sxs-lookup"><span data-stu-id="41d1d-129"><span id="0x80040xxx"></span><span id="0X80040XXX"></span>0x80040xxx</span></span>
</dt> <dd>

<span data-ttu-id="41d1d-130">Erros originados no DCOM.</span><span class="sxs-lookup"><span data-stu-id="41d1d-130">Errors originating in DCOM.</span></span> <span data-ttu-id="41d1d-131">Por exemplo, a configuração de DCOM para operações em um computador remoto pode estar incorreta.</span><span class="sxs-lookup"><span data-stu-id="41d1d-131">For example, the DCOM configuration for operations to a remote computer may be incorrect.</span></span>

</dd> <dt>

<span data-ttu-id="41d1d-132"><span id="0x8005xxxx"></span><span id="0X8005XXXX"></span>0x8005xxxx</span><span class="sxs-lookup"><span data-stu-id="41d1d-132"><span id="0x8005xxxx"></span><span id="0X8005XXXX"></span>0x8005xxxx</span></span>
</dt> <dd>

<span data-ttu-id="41d1d-133">Erro originado de ADSI (Active Directory interfaces de serviço) ou LDAP (Lightweight Directory Access Protocol), por exemplo, uma falha de acesso de Active Directory ao usar os provedores de Active Directory do WMI.</span><span class="sxs-lookup"><span data-stu-id="41d1d-133">Error originating from ADSI (Active Directory Service Interfaces) or LDAP (Lightweight Directory Access Protocol), for example, an Active Directory access failure when using the WMI Active Directory providers.</span></span>

</dd> </dl>

<span data-ttu-id="41d1d-134">Alguns métodos em classes WMI podem retornar códigos de erro de sistema e rede (64, por exemplo).</span><span class="sxs-lookup"><span data-stu-id="41d1d-134">Some methods in WMI classes can return system and network error codes (64 for example).</span></span> <span data-ttu-id="41d1d-135">Você pode verificar a definição desses tipos de códigos de erro usando o comando **net helpmsg** na janela do prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="41d1d-135">You can check the definition of these types of error codes by using the **net helpmsg** command in the command prompt window.</span></span> <span data-ttu-id="41d1d-136">Por exemplo, o comando **net helpmsg 64** retorna a mensagem: o nome de rede especificado não está mais disponível.</span><span class="sxs-lookup"><span data-stu-id="41d1d-136">For example, the command **net helpmsg 64** returns the message: The specified network name is no longer available.</span></span> <span data-ttu-id="41d1d-137">Em C++, você pode chamar [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) e especificar **C: \\ Windows \\ System32 \\ WBEM \\wmiutils.dll** como o módulo de mensagem.</span><span class="sxs-lookup"><span data-stu-id="41d1d-137">In C++, you can call [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) and specify **C:\\Windows\\System32\\wbem\\wmiutils.dll** as the message module.</span></span>

<dl> <dt>

<span data-ttu-id="41d1d-138"><span id="WBEM_E_FAILED"></span><span id="wbem_e_failed"></span>**falha de WBEM \_ E \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-138"><span id="WBEM_E_FAILED"></span><span id="wbem_e_failed"></span>**WBEM\_E\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-139">2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="41d1d-139">2147749889 (0x80041001)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-140">Falha na chamada.</span><span class="sxs-lookup"><span data-stu-id="41d1d-140">Call failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-141"><span id="WBEM_E_NOT_FOUND"></span><span id="wbem_e_not_found"></span>**WBEM \_ E \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="41d1d-141"><span id="WBEM_E_NOT_FOUND"></span><span id="wbem_e_not_found"></span>**WBEM\_E\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-142">2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="41d1d-142">2147749890 (0x80041002)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-143">Objeto não encontrado.</span><span class="sxs-lookup"><span data-stu-id="41d1d-143">Object cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-144"><span id="WBEM_E_ACCESS_DENIED"></span><span id="wbem_e_access_denied"></span>**acesso ao WBEM \_ E \_ \_ negado**</span><span class="sxs-lookup"><span data-stu-id="41d1d-144"><span id="WBEM_E_ACCESS_DENIED"></span><span id="wbem_e_access_denied"></span>**WBEM\_E\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-145">2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="41d1d-145">2147749891 (0x80041003)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-146">O usuário atual não tem permissão para executar a ação.</span><span class="sxs-lookup"><span data-stu-id="41d1d-146">Current user does not have permission to perform the action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-147"><span id="WBEM_E_PROVIDER_FAILURE"></span><span id="wbem_e_provider_failure"></span>**\_falha do \_ provedor WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-147"><span id="WBEM_E_PROVIDER_FAILURE"></span><span id="wbem_e_provider_failure"></span>**WBEM\_E\_PROVIDER\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-148">2147749892 (0x80041004)</span><span class="sxs-lookup"><span data-stu-id="41d1d-148">2147749892 (0x80041004)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-149">O provedor falhou em algum momento diferente durante a inicialização.</span><span class="sxs-lookup"><span data-stu-id="41d1d-149">Provider has failed at some time other than during initialization.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-150"><span id="WBEM_E_TYPE_MISMATCH"></span><span id="wbem_e_type_mismatch"></span>**incompatibilidade de \_ tipo WBEM E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-150"><span id="WBEM_E_TYPE_MISMATCH"></span><span id="wbem_e_type_mismatch"></span>**WBEM\_E\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-151">2147749893 (0x80041005)</span><span class="sxs-lookup"><span data-stu-id="41d1d-151">2147749893 (0x80041005)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-152">Erro de incompatibilidade de tipo.</span><span class="sxs-lookup"><span data-stu-id="41d1d-152">Type mismatch occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-153"><span id="WBEM_E_OUT_OF_MEMORY"></span><span id="wbem_e_out_of_memory"></span>**WBEM \_ E \_ memória insuficiente \_ \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-153"><span id="WBEM_E_OUT_OF_MEMORY"></span><span id="wbem_e_out_of_memory"></span>**WBEM\_E\_OUT\_OF\_MEMORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-154">2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="41d1d-154">2147749894 (0x80041006)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-155">Não há memória suficiente para a operação.</span><span class="sxs-lookup"><span data-stu-id="41d1d-155">Not enough memory for the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-156"><span id="WBEM_E_INVALID_CONTEXT"></span><span id="wbem_e_invalid_context"></span>**\_ \_ contexto inválido do WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-156"><span id="WBEM_E_INVALID_CONTEXT"></span><span id="wbem_e_invalid_context"></span>**WBEM\_E\_INVALID\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-157">2147749895 (0x80041007)</span><span class="sxs-lookup"><span data-stu-id="41d1d-157">2147749895 (0x80041007)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-158">O objeto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) não é válido.</span><span class="sxs-lookup"><span data-stu-id="41d1d-158">The [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-159"><span id="WBEM_E_INVALID_PARAMETER"></span><span id="wbem_e_invalid_parameter"></span>**parâmetro de WBEM \_ E \_ inválido \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-159"><span id="WBEM_E_INVALID_PARAMETER"></span><span id="wbem_e_invalid_parameter"></span>**WBEM\_E\_INVALID\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-160">2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="41d1d-160">2147749896 (0x80041008)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-161">Um dos parâmetros para a chamada não está correto.</span><span class="sxs-lookup"><span data-stu-id="41d1d-161">One of the parameters to the call is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-162"><span id="WBEM_E_NOT_AVAILABLE"></span><span id="wbem_e_not_available"></span>**WBEM \_ E \_ não \_ disponível**</span><span class="sxs-lookup"><span data-stu-id="41d1d-162"><span id="WBEM_E_NOT_AVAILABLE"></span><span id="wbem_e_not_available"></span>**WBEM\_E\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-163">2147749897 (0x80041009)</span><span class="sxs-lookup"><span data-stu-id="41d1d-163">2147749897 (0x80041009)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-164">O recurso, normalmente um servidor remoto, não está disponível no momento.</span><span class="sxs-lookup"><span data-stu-id="41d1d-164">Resource, typically a remote server, is not currently available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-165"><span id="WBEM_E_CRITICAL_ERROR"></span><span id="wbem_e_critical_error"></span>**\_ \_ erro crítico de WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-165"><span id="WBEM_E_CRITICAL_ERROR"></span><span id="wbem_e_critical_error"></span>**WBEM\_E\_CRITICAL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-166">2147749898 (0x8004100A)</span><span class="sxs-lookup"><span data-stu-id="41d1d-166">2147749898 (0x8004100A)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-167">Ocorreu um erro interno, crítico e inesperado.</span><span class="sxs-lookup"><span data-stu-id="41d1d-167">Internal, critical, and unexpected error occurred.</span></span> <span data-ttu-id="41d1d-168">Relate o erro ao suporte técnico da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="41d1d-168">Report the error to Microsoft Technical Support.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-169"><span id="WBEM_E_INVALID_STREAM"></span><span id="wbem_e_invalid_stream"></span>**\_ \_ fluxo inválido do WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-169"><span id="WBEM_E_INVALID_STREAM"></span><span id="wbem_e_invalid_stream"></span>**WBEM\_E\_INVALID\_STREAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-170">2147749899 (0x8004100B)</span><span class="sxs-lookup"><span data-stu-id="41d1d-170">2147749899 (0x8004100B)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-171">Um ou mais pacotes de rede foram corrompidos durante uma sessão remota.</span><span class="sxs-lookup"><span data-stu-id="41d1d-171">One or more network packets were corrupted during a remote session.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-172"><span id="WBEM_E_NOT_SUPPORTED"></span><span id="wbem_e_not_supported"></span>**\_ \_ não \_ há suporte para o WBEM E**</span><span class="sxs-lookup"><span data-stu-id="41d1d-172"><span id="WBEM_E_NOT_SUPPORTED"></span><span id="wbem_e_not_supported"></span>**WBEM\_E\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-173">2147749900 (0x8004100C)</span><span class="sxs-lookup"><span data-stu-id="41d1d-173">2147749900 (0x8004100C)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-174">Não há suporte para o recurso ou operação.</span><span class="sxs-lookup"><span data-stu-id="41d1d-174">Feature or operation is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-175"><span id="WBEM_E_INVALID_SUPERCLASS"></span><span id="wbem_e_invalid_superclass"></span>**superclasse WBEM \_ E \_ inválido \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-175"><span id="WBEM_E_INVALID_SUPERCLASS"></span><span id="wbem_e_invalid_superclass"></span>**WBEM\_E\_INVALID\_SUPERCLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-176">2147749901 (0x8004100D)</span><span class="sxs-lookup"><span data-stu-id="41d1d-176">2147749901 (0x8004100D)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-177">A classe pai especificada não é válida.</span><span class="sxs-lookup"><span data-stu-id="41d1d-177">Parent class specified is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-178"><span id="WBEM_E_INVALID_NAMESPACE"></span><span id="wbem_e_invalid_namespace"></span>**WBEM \_ E \_ \_ namespace inválido**</span><span class="sxs-lookup"><span data-stu-id="41d1d-178"><span id="WBEM_E_INVALID_NAMESPACE"></span><span id="wbem_e_invalid_namespace"></span>**WBEM\_E\_INVALID\_NAMESPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-179">2147749902 (0x8004100E)</span><span class="sxs-lookup"><span data-stu-id="41d1d-179">2147749902 (0x8004100E)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-180">O namespace especificado não pode ser encontrado.</span><span class="sxs-lookup"><span data-stu-id="41d1d-180">Namespace specified cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-181"><span id="WBEM_E_INVALID_OBJECT"></span><span id="wbem_e_invalid_object"></span>**\_objeto WBEM E \_ inválido \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-181"><span id="WBEM_E_INVALID_OBJECT"></span><span id="wbem_e_invalid_object"></span>**WBEM\_E\_INVALID\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-182">2147749903 (0x8004100F)</span><span class="sxs-lookup"><span data-stu-id="41d1d-182">2147749903 (0x8004100F)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-183">A instância especificada não é válida.</span><span class="sxs-lookup"><span data-stu-id="41d1d-183">Specified instance is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-184"><span id="WBEM_E_INVALID_CLASS"></span><span id="wbem_e_invalid_class"></span>**\_classe WBEM E \_ inválida \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-184"><span id="WBEM_E_INVALID_CLASS"></span><span id="wbem_e_invalid_class"></span>**WBEM\_E\_INVALID\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-185">2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="41d1d-185">2147749904 (0x80041010)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-186">A classe especificada não é válida.</span><span class="sxs-lookup"><span data-stu-id="41d1d-186">Specified class is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-187"><span id="WBEM_E_PROVIDER_NOT_FOUND"></span><span id="wbem_e_provider_not_found"></span>**\_provedor WBEM \_ E \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="41d1d-187"><span id="WBEM_E_PROVIDER_NOT_FOUND"></span><span id="wbem_e_provider_not_found"></span>**WBEM\_E\_PROVIDER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-188">2147749905 (0x80041011)</span><span class="sxs-lookup"><span data-stu-id="41d1d-188">2147749905 (0x80041011)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-189">O provedor referenciado no esquema não tem um registro correspondente.</span><span class="sxs-lookup"><span data-stu-id="41d1d-189">Provider referenced in the schema does not have a corresponding registration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-190"><span id="WBEM_E_INVALID_PROVIDER_REGISTRATION"></span><span id="wbem_e_invalid_provider_registration"></span>**WBEM \_ E \_ \_ registro de provedor inválido \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-190"><span id="WBEM_E_INVALID_PROVIDER_REGISTRATION"></span><span id="wbem_e_invalid_provider_registration"></span>**WBEM\_E\_INVALID\_PROVIDER\_REGISTRATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-191">2147749906</span><span class="sxs-lookup"><span data-stu-id="41d1d-191">2147749906</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-192">O provedor referenciado no esquema tem um registro incorreto ou incompleto.</span><span class="sxs-lookup"><span data-stu-id="41d1d-192">Provider referenced in the schema has an incorrect or incomplete registration.</span></span>

<span data-ttu-id="41d1d-193">Esse erro pode ser causado por muitas condições, incluindo as seguintes:</span><span class="sxs-lookup"><span data-stu-id="41d1d-193">This error may be caused by many conditions, including the following:</span></span>

-   <span data-ttu-id="41d1d-194">Um comando de [ \# namespace de pragma](pragma-namespace.md) ausente no arquivo de formato MOF (MOF) usado para registrar o provedor.</span><span class="sxs-lookup"><span data-stu-id="41d1d-194">A missing [\#pragma namespace](pragma-namespace.md) command in the Managed Object Format (MOF) file used to register the provider.</span></span> <span data-ttu-id="41d1d-195">O provedor pode ser registrado no namespace WMI errado.</span><span class="sxs-lookup"><span data-stu-id="41d1d-195">The provider may be registered in the wrong WMI namespace.</span></span>
-   <span data-ttu-id="41d1d-196">Falha ao recuperar o registro COM.</span><span class="sxs-lookup"><span data-stu-id="41d1d-196">Failure to retrieve the COM registration.</span></span>
-   <span data-ttu-id="41d1d-197">O modelo de hospedagem não é válido.</span><span class="sxs-lookup"><span data-stu-id="41d1d-197">Hosting model is not valid.</span></span> <span data-ttu-id="41d1d-198">Para obter mais informações, consulte [provedor de hospedagem e segurança](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="41d1d-198">For more information, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>
-   <span data-ttu-id="41d1d-199">Uma classe especificada no registro não é válida.</span><span class="sxs-lookup"><span data-stu-id="41d1d-199">An class specified in the registration is not valid.</span></span>
-   <span data-ttu-id="41d1d-200">Falha ao criar uma instância do ou herdar da classe [**\_ \_ Win32Provider**](--win32provider.md) para criar o registro do provedor no arquivo MOF.</span><span class="sxs-lookup"><span data-stu-id="41d1d-200">Failure to create an instance of or inherit from the [**\_\_Win32Provider**](--win32provider.md) class to create the provider registration in the MOF file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-201"><span id="WBEM_E_PROVIDER_LOAD_FAILURE"></span><span id="wbem_e_provider_load_failure"></span>**\_falha de \_ carregamento do provedor WBEM E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-201"><span id="WBEM_E_PROVIDER_LOAD_FAILURE"></span><span id="wbem_e_provider_load_failure"></span>**WBEM\_E\_PROVIDER\_LOAD\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-202">2147749907 (0x80041013)</span><span class="sxs-lookup"><span data-stu-id="41d1d-202">2147749907 (0x80041013)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-203">COM não pode localizar um provedor referenciado no esquema.</span><span class="sxs-lookup"><span data-stu-id="41d1d-203">COM cannot locate a provider referenced in the schema.</span></span>

<span data-ttu-id="41d1d-204">Esse erro pode ser causado por muitas condições, incluindo as seguintes:</span><span class="sxs-lookup"><span data-stu-id="41d1d-204">This error may be caused by many conditions, including the following:</span></span>

-   <span data-ttu-id="41d1d-205">O provedor está usando uma DLL WMI que não corresponde ao arquivo. lib usado quando o provedor foi criado.</span><span class="sxs-lookup"><span data-stu-id="41d1d-205">Provider is using a WMI DLL that does not match the .lib file used when the provider was built.</span></span>
-   <span data-ttu-id="41d1d-206">A DLL do provedor, ou qualquer uma das DLLs das quais ela depende, está corrompida.</span><span class="sxs-lookup"><span data-stu-id="41d1d-206">Provider's DLL, or any of the DLLs on which it depends, is corrupt.</span></span>
-   <span data-ttu-id="41d1d-207">Falha do provedor ao exportar [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver).</span><span class="sxs-lookup"><span data-stu-id="41d1d-207">Provider failed to export [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver).</span></span>
-   <span data-ttu-id="41d1d-208">O provedor em processo não foi registrado usando o comando **regsvr32** .</span><span class="sxs-lookup"><span data-stu-id="41d1d-208">In-process provider was not registered using the **regsvr32** command.</span></span>
-   <span data-ttu-id="41d1d-209">O provedor fora do processo não foi registrado usando a opção **/RegServer** .</span><span class="sxs-lookup"><span data-stu-id="41d1d-209">Out-of-process provider was not registered using the **/regserver** switch.</span></span> <span data-ttu-id="41d1d-210">Por exemplo, **myprog.exe/RegServer**.</span><span class="sxs-lookup"><span data-stu-id="41d1d-210">For example, **myprog.exe /regserver**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-211"><span id="WBEM_E_INITIALIZATION_FAILURE"></span><span id="wbem_e_initialization_failure"></span>**\_ \_ falha na inicialização do WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-211"><span id="WBEM_E_INITIALIZATION_FAILURE"></span><span id="wbem_e_initialization_failure"></span>**WBEM\_E\_INITIALIZATION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-212">2147749908 (0x80041014)</span><span class="sxs-lookup"><span data-stu-id="41d1d-212">2147749908 (0x80041014)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-213">O componente, como um provedor, não pôde ser inicializado por motivos internos.</span><span class="sxs-lookup"><span data-stu-id="41d1d-213">Component, such as a provider, failed to initialize for internal reasons.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-214"><span id="WBEM_E_TRANSPORT_FAILURE"></span><span id="wbem_e_transport_failure"></span>**\_falha de \_ transporte \_ E de WBEM**</span><span class="sxs-lookup"><span data-stu-id="41d1d-214"><span id="WBEM_E_TRANSPORT_FAILURE"></span><span id="wbem_e_transport_failure"></span>**WBEM\_E\_TRANSPORT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-215">2147749909 (0x80041015)</span><span class="sxs-lookup"><span data-stu-id="41d1d-215">2147749909 (0x80041015)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-216">Erro de rede que impede que a operação normal ocorra.</span><span class="sxs-lookup"><span data-stu-id="41d1d-216">Networking error that prevents normal operation has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-217"><span id="WBEM_E_INVALID_OPERATION"></span><span id="wbem_e_invalid_operation"></span>**operação de WBEM \_ E \_ inválida \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-217"><span id="WBEM_E_INVALID_OPERATION"></span><span id="wbem_e_invalid_operation"></span>**WBEM\_E\_INVALID\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-218">2147749910 (0x80041016)</span><span class="sxs-lookup"><span data-stu-id="41d1d-218">2147749910 (0x80041016)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-219">A operação solicitada não é válida.</span><span class="sxs-lookup"><span data-stu-id="41d1d-219">Requested operation is not valid.</span></span> <span data-ttu-id="41d1d-220">Esse erro geralmente se aplica a tentativas inválidas para excluir classes ou propriedades.</span><span class="sxs-lookup"><span data-stu-id="41d1d-220">This error usually applies to invalid attempts to delete classes or properties.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-221"><span id="WBEM_E_INVALID_QUERY"></span><span id="wbem_e_invalid_query"></span>**WBEM \_ E \_ consulta inválida \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-221"><span id="WBEM_E_INVALID_QUERY"></span><span id="wbem_e_invalid_query"></span>**WBEM\_E\_INVALID\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-222">2147749911 (0x80041017)</span><span class="sxs-lookup"><span data-stu-id="41d1d-222">2147749911 (0x80041017)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-223">A consulta não era sintaticamente válida.</span><span class="sxs-lookup"><span data-stu-id="41d1d-223">Query was not syntactically valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-224"><span id="WBEM_E_INVALID_QUERY_TYPE"></span><span id="wbem_e_invalid_query_type"></span>**\_tipo de consulta WBEM E \_ inválido \_ \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-224"><span id="WBEM_E_INVALID_QUERY_TYPE"></span><span id="wbem_e_invalid_query_type"></span>**WBEM\_E\_INVALID\_QUERY\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-225">2147749912 (0x80041018)</span><span class="sxs-lookup"><span data-stu-id="41d1d-225">2147749912 (0x80041018)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-226">Não há suporte para a linguagem de consulta solicitada.</span><span class="sxs-lookup"><span data-stu-id="41d1d-226">Requested query language is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-227"><span id="WBEM_E_ALREADY_EXISTS"></span><span id="wbem_e_already_exists"></span>**o WBEM \_ E \_ já \_ existe**</span><span class="sxs-lookup"><span data-stu-id="41d1d-227"><span id="WBEM_E_ALREADY_EXISTS"></span><span id="wbem_e_already_exists"></span>**WBEM\_E\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-228">2147749913 (0x80041019)</span><span class="sxs-lookup"><span data-stu-id="41d1d-228">2147749913 (0x80041019)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-229">Em uma operação put, o sinalizador **wbemChangeFlagCreateOnly** foi especificado, mas a instância já existe.</span><span class="sxs-lookup"><span data-stu-id="41d1d-229">In a put operation, the **wbemChangeFlagCreateOnly** flag was specified, but the instance already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-230"><span id="WBEM_E_OVERRIDE_NOT_ALLOWED"></span><span id="wbem_e_override_not_allowed"></span>**substituição de WBEM \_ E \_ \_ não \_ permitida**</span><span class="sxs-lookup"><span data-stu-id="41d1d-230"><span id="WBEM_E_OVERRIDE_NOT_ALLOWED"></span><span id="wbem_e_override_not_allowed"></span>**WBEM\_E\_OVERRIDE\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-231">2147749914 (0x8004101A)</span><span class="sxs-lookup"><span data-stu-id="41d1d-231">2147749914 (0x8004101A)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-232">Não é possível executar a operação de adição neste qualificador porque o objeto proprietário não permite substituições.</span><span class="sxs-lookup"><span data-stu-id="41d1d-232">Not possible to perform the add operation on this qualifier because the owning object does not permit overrides.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-233"><span id="WBEM_E_PROPAGATED_QUALIFIER"></span><span id="wbem_e_propagated_qualifier"></span>**\_qualificador do WBEM E \_ propagado \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-233"><span id="WBEM_E_PROPAGATED_QUALIFIER"></span><span id="wbem_e_propagated_qualifier"></span>**WBEM\_E\_PROPAGATED\_QUALIFIER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-234">2147749915 (0x8004101B)</span><span class="sxs-lookup"><span data-stu-id="41d1d-234">2147749915 (0x8004101B)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-235">O usuário tentou excluir um qualificador que não era de propriedade.</span><span class="sxs-lookup"><span data-stu-id="41d1d-235">User attempted to delete a qualifier that was not owned.</span></span> <span data-ttu-id="41d1d-236">O qualificador foi herdado de uma classe pai.</span><span class="sxs-lookup"><span data-stu-id="41d1d-236">The qualifier was inherited from a parent class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-237"><span id="WBEM_E_PROPAGATED_PROPERTY"></span><span id="wbem_e_propagated_property"></span>**Propriedade de WBEM \_ E \_ propagada \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-237"><span id="WBEM_E_PROPAGATED_PROPERTY"></span><span id="wbem_e_propagated_property"></span>**WBEM\_E\_PROPAGATED\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-238">2147749916 (0x8004101C)</span><span class="sxs-lookup"><span data-stu-id="41d1d-238">2147749916 (0x8004101C)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-239">O usuário tentou excluir uma propriedade que não era de propriedade.</span><span class="sxs-lookup"><span data-stu-id="41d1d-239">User attempted to delete a property that was not owned.</span></span> <span data-ttu-id="41d1d-240">A propriedade foi herdada de uma classe pai.</span><span class="sxs-lookup"><span data-stu-id="41d1d-240">The property was inherited from a parent class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-241"><span id="WBEM_E_UNEXPECTED"></span><span id="wbem_e_unexpected"></span>**WBEM \_ E \_ inesperado**</span><span class="sxs-lookup"><span data-stu-id="41d1d-241"><span id="WBEM_E_UNEXPECTED"></span><span id="wbem_e_unexpected"></span>**WBEM\_E\_UNEXPECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-242">2147749917 (0x8004101D)</span><span class="sxs-lookup"><span data-stu-id="41d1d-242">2147749917 (0x8004101D)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-243">O cliente fez uma sequência de chamadas inesperada e ilegal, como chamar [**Endenumeration**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-endenumeration) antes de chamar [**BeginEnumeration**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-beginenumeration).</span><span class="sxs-lookup"><span data-stu-id="41d1d-243">Client made an unexpected and illegal sequence of calls, such as calling [**EndEnumeration**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-endenumeration) before calling [**BeginEnumeration**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-beginenumeration).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-244"><span id="WBEM_E_ILLEGAL_OPERATION"></span><span id="wbem_e_illegal_operation"></span>**operação de WBEM \_ E \_ ilegal \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-244"><span id="WBEM_E_ILLEGAL_OPERATION"></span><span id="wbem_e_illegal_operation"></span>**WBEM\_E\_ILLEGAL\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-245">2147749918 (0x8004101E)</span><span class="sxs-lookup"><span data-stu-id="41d1d-245">2147749918 (0x8004101E)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-246">O usuário solicitou uma operação ilegal, como a geração de uma classe de uma instância.</span><span class="sxs-lookup"><span data-stu-id="41d1d-246">User requested an illegal operation, such as spawning a class from an instance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-247"><span id="WBEM_E_CANNOT_BE_KEY"></span><span id="wbem_e_cannot_be_key"></span>**WBEM \_ E \_ não podem \_ ser \_ chave**</span><span class="sxs-lookup"><span data-stu-id="41d1d-247"><span id="WBEM_E_CANNOT_BE_KEY"></span><span id="wbem_e_cannot_be_key"></span>**WBEM\_E\_CANNOT\_BE\_KEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-248">2147749919 (0x8004101F)</span><span class="sxs-lookup"><span data-stu-id="41d1d-248">2147749919 (0x8004101F)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-249">Tentativa inválida de especificar um qualificador de chave em uma propriedade que não pode ser uma chave.</span><span class="sxs-lookup"><span data-stu-id="41d1d-249">Illegal attempt to specify a key qualifier on a property that cannot be a key.</span></span> <span data-ttu-id="41d1d-250">As chaves são especificadas na definição de classe para um objeto e não podem ser alteradas por instância.</span><span class="sxs-lookup"><span data-stu-id="41d1d-250">The keys are specified in the class definition for an object and cannot be altered on a per-instance basis.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-251"><span id="WBEM_E_INCOMPLETE_CLASS"></span><span id="wbem_e_incomplete_class"></span>**\_classe WBEM E \_ incompleta \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-251"><span id="WBEM_E_INCOMPLETE_CLASS"></span><span id="wbem_e_incomplete_class"></span>**WBEM\_E\_INCOMPLETE\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-252">2147749920 (0x80041020)</span><span class="sxs-lookup"><span data-stu-id="41d1d-252">2147749920 (0x80041020)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-253">O objeto atual não é uma definição de classe válida.</span><span class="sxs-lookup"><span data-stu-id="41d1d-253">Current object is not a valid class definition.</span></span> <span data-ttu-id="41d1d-254">Ele está incompleto ou não foi registrado com WMI usando [**SWbemObject. put \_**](swbemobject-put-.md).</span><span class="sxs-lookup"><span data-stu-id="41d1d-254">Either it is incomplete or it has not been registered with WMI using [**SWbemObject.Put\_**](swbemobject-put-.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-255"><span id="WBEM_E_INVALID_SYNTAX"></span><span id="wbem_e_invalid_syntax"></span>**sintaxe de WBEM \_ E \_ inválida \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-255"><span id="WBEM_E_INVALID_SYNTAX"></span><span id="wbem_e_invalid_syntax"></span>**WBEM\_E\_INVALID\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-256">2147749921 (0x80041021)</span><span class="sxs-lookup"><span data-stu-id="41d1d-256">2147749921 (0x80041021)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-257">A consulta é sintaticamente inválida.</span><span class="sxs-lookup"><span data-stu-id="41d1d-257">Query is syntactically not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-258"><span id="WBEM_E_NONDECORATED_OBJECT"></span><span id="wbem_e_nondecorated_object"></span>**\_objeto WBEM E não \_ decorado \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-258"><span id="WBEM_E_NONDECORATED_OBJECT"></span><span id="wbem_e_nondecorated_object"></span>**WBEM\_E\_NONDECORATED\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-259">2147749922 (0x80041022)</span><span class="sxs-lookup"><span data-stu-id="41d1d-259">2147749922 (0x80041022)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-260">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="41d1d-260">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-261"><span id="WBEM_E_READ_ONLY"></span><span id="wbem_e_read_only"></span>**WBEM \_ E \_ \_ somente leitura**</span><span class="sxs-lookup"><span data-stu-id="41d1d-261"><span id="WBEM_E_READ_ONLY"></span><span id="wbem_e_read_only"></span>**WBEM\_E\_READ\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-262">2147749923 (0x80041023)</span><span class="sxs-lookup"><span data-stu-id="41d1d-262">2147749923 (0x80041023)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-263">Foi feita uma tentativa de modificar uma propriedade somente leitura.</span><span class="sxs-lookup"><span data-stu-id="41d1d-263">An attempt was made to modify a read-only property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-264"><span id="WBEM_E_PROVIDER_NOT_CAPABLE"></span><span id="wbem_e_provider_not_capable"></span>**\_provedor WBEM \_ E \_ não \_ compatível**</span><span class="sxs-lookup"><span data-stu-id="41d1d-264"><span id="WBEM_E_PROVIDER_NOT_CAPABLE"></span><span id="wbem_e_provider_not_capable"></span>**WBEM\_E\_PROVIDER\_NOT\_CAPABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-265">2147749924 (0x80041024)</span><span class="sxs-lookup"><span data-stu-id="41d1d-265">2147749924 (0x80041024)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-266">O provedor não pode executar a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="41d1d-266">Provider cannot perform the requested operation.</span></span> <span data-ttu-id="41d1d-267">Isso pode incluir uma consulta que seja muito complexa, recuperando uma instância, criando ou atualizando uma classe, excluindo uma classe ou enumerando uma classe.</span><span class="sxs-lookup"><span data-stu-id="41d1d-267">This can include a query that is too complex, retrieving an instance, creating or updating a class, deleting a class, or enumerating a class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-268"><span id="WBEM_E_CLASS_HAS_CHILDREN"></span><span id="wbem_e_class_has_children"></span>**a \_ classe WBEM E \_ \_ tem \_ filhos**</span><span class="sxs-lookup"><span data-stu-id="41d1d-268"><span id="WBEM_E_CLASS_HAS_CHILDREN"></span><span id="wbem_e_class_has_children"></span>**WBEM\_E\_CLASS\_HAS\_CHILDREN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-269">2147749925 (0x80041025)</span><span class="sxs-lookup"><span data-stu-id="41d1d-269">2147749925 (0x80041025)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-270">Foi feita uma tentativa de fazer uma alteração que invalida uma subclasse.</span><span class="sxs-lookup"><span data-stu-id="41d1d-270">Attempt was made to make a change that invalidates a subclass.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-271"><span id="WBEM_E_CLASS_HAS_INSTANCES"></span><span id="wbem_e_class_has_instances"></span>**\_classe WBEM \_ E \_ possui \_ instâncias**</span><span class="sxs-lookup"><span data-stu-id="41d1d-271"><span id="WBEM_E_CLASS_HAS_INSTANCES"></span><span id="wbem_e_class_has_instances"></span>**WBEM\_E\_CLASS\_HAS\_INSTANCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-272">2147749926 (0x80041026)</span><span class="sxs-lookup"><span data-stu-id="41d1d-272">2147749926 (0x80041026)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-273">Foi feita uma tentativa de excluir ou modificar uma classe que tem instâncias.</span><span class="sxs-lookup"><span data-stu-id="41d1d-273">Attempt was made to delete or modify a class that has instances.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-274"><span id="WBEM_E_QUERY_NOT_IMPLEMENTED"></span><span id="wbem_e_query_not_implemented"></span>**\_consulta WBEM \_ E \_ não \_ implementada**</span><span class="sxs-lookup"><span data-stu-id="41d1d-274"><span id="WBEM_E_QUERY_NOT_IMPLEMENTED"></span><span id="wbem_e_query_not_implemented"></span>**WBEM\_E\_QUERY\_NOT\_IMPLEMENTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-275">2147749927 (0x80041027)</span><span class="sxs-lookup"><span data-stu-id="41d1d-275">2147749927 (0x80041027)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-276">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="41d1d-276">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-277"><span id="WBEM_E_ILLEGAL_NULL"></span><span id="wbem_e_illegal_null"></span>**WBEM \_ E \_ \_ nulo inválido**</span><span class="sxs-lookup"><span data-stu-id="41d1d-277"><span id="WBEM_E_ILLEGAL_NULL"></span><span id="wbem_e_illegal_null"></span>**WBEM\_E\_ILLEGAL\_NULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-278">2147749928 (0x80041028)</span><span class="sxs-lookup"><span data-stu-id="41d1d-278">2147749928 (0x80041028)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-279">O valor de Nothing/**NULL** foi especificado para uma propriedade que deve ter um valor, como um que é marcado por um qualificador de [**chave**](key-qualifier.md), [**indexado**](optional-qualifiers.md)ou **não \_ nulo** .</span><span class="sxs-lookup"><span data-stu-id="41d1d-279">Value of Nothing/**NULL** was specified for a property that must have a value, such as one that is marked by a [**Key**](key-qualifier.md), [**Indexed**](optional-qualifiers.md), or **Not\_Null** qualifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-280"><span id="WBEM_E_INVALID_QUALIFIER_TYPE"></span><span id="wbem_e_invalid_qualifier_type"></span>**\_tipo de \_ \_ qualificador E inválido \_ do WBEM**</span><span class="sxs-lookup"><span data-stu-id="41d1d-280"><span id="WBEM_E_INVALID_QUALIFIER_TYPE"></span><span id="wbem_e_invalid_qualifier_type"></span>**WBEM\_E\_INVALID\_QUALIFIER\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-281">2147749929 (0x80041029)</span><span class="sxs-lookup"><span data-stu-id="41d1d-281">2147749929 (0x80041029)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-282">Foi fornecido um valor de variante para um qualificador que não é um tipo de qualificador legal.</span><span class="sxs-lookup"><span data-stu-id="41d1d-282">Variant value for a qualifier was provided that is not a legal qualifier type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-283"><span id="WBEM_E_INVALID_PROPERTY_TYPE"></span><span id="wbem_e_invalid_property_type"></span>**tipo de propriedade de WBEM \_ E \_ inválido \_ \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-283"><span id="WBEM_E_INVALID_PROPERTY_TYPE"></span><span id="wbem_e_invalid_property_type"></span>**WBEM\_E\_INVALID\_PROPERTY\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-284">2147749930 (0x8004102A)</span><span class="sxs-lookup"><span data-stu-id="41d1d-284">2147749930 (0x8004102A)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-285">O tipo CIM especificado para uma propriedade não é válido.</span><span class="sxs-lookup"><span data-stu-id="41d1d-285">CIM type specified for a property is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-286"><span id="WBEM_E_VALUE_OUT_OF_RANGE"></span><span id="wbem_e_value_out_of_range"></span>**WBEM \_ E \_ valor \_ fora \_ do \_ intervalo**</span><span class="sxs-lookup"><span data-stu-id="41d1d-286"><span id="WBEM_E_VALUE_OUT_OF_RANGE"></span><span id="wbem_e_value_out_of_range"></span>**WBEM\_E\_VALUE\_OUT\_OF\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-287">2147749931 (0x8004102B)</span><span class="sxs-lookup"><span data-stu-id="41d1d-287">2147749931 (0x8004102B)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-288">A solicitação foi feita com um valor fora do intervalo ou é incompatível com o tipo.</span><span class="sxs-lookup"><span data-stu-id="41d1d-288">Request was made with an out-of-range value or it is incompatible with the type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-289"><span id="WBEM_E_CANNOT_BE_SINGLETON"></span><span id="wbem_e_cannot_be_singleton"></span>**WBEM \_ E \_ não podem \_ ser \_ singleton**</span><span class="sxs-lookup"><span data-stu-id="41d1d-289"><span id="WBEM_E_CANNOT_BE_SINGLETON"></span><span id="wbem_e_cannot_be_singleton"></span>**WBEM\_E\_CANNOT\_BE\_SINGLETON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-290">2147749932 (0x8004102C)</span><span class="sxs-lookup"><span data-stu-id="41d1d-290">2147749932 (0x8004102C)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-291">Foi feita uma tentativa ilegal de tornar uma classe singleton, como quando a classe é derivada de uma classe não singleton.</span><span class="sxs-lookup"><span data-stu-id="41d1d-291">Illegal attempt was made to make a class singleton, such as when the class is derived from a non-singleton class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-292"><span id="WBEM_E_INVALID_CIM_TYPE"></span><span id="wbem_e_invalid_cim_type"></span>**WBEM \_ E \_ \_ tipo CIM \_ inválido**</span><span class="sxs-lookup"><span data-stu-id="41d1d-292"><span id="WBEM_E_INVALID_CIM_TYPE"></span><span id="wbem_e_invalid_cim_type"></span>**WBEM\_E\_INVALID\_CIM\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-293">2147749933 (0x8004102D)</span><span class="sxs-lookup"><span data-stu-id="41d1d-293">2147749933 (0x8004102D)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-294">O tipo CIM especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="41d1d-294">CIM type specified is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-295"><span id="WBEM_E_INVALID_METHOD"></span><span id="wbem_e_invalid_method"></span>**\_ \_ método inválido do WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-295"><span id="WBEM_E_INVALID_METHOD"></span><span id="wbem_e_invalid_method"></span>**WBEM\_E\_INVALID\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-296">2147749934 (0x8004102E)</span><span class="sxs-lookup"><span data-stu-id="41d1d-296">2147749934 (0x8004102E)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-297">O método solicitado não está disponível.</span><span class="sxs-lookup"><span data-stu-id="41d1d-297">Requested method is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-298"><span id="WBEM_E_INVALID_METHOD_PARAMETERS"></span><span id="wbem_e_invalid_method_parameters"></span>**\_parâmetros de \_ \_ método inválido E WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-298"><span id="WBEM_E_INVALID_METHOD_PARAMETERS"></span><span id="wbem_e_invalid_method_parameters"></span>**WBEM\_E\_INVALID\_METHOD\_PARAMETERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-299">2147749935 (0x8004102F)</span><span class="sxs-lookup"><span data-stu-id="41d1d-299">2147749935 (0x8004102F)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-300">Os parâmetros fornecidos para o método não são válidos.</span><span class="sxs-lookup"><span data-stu-id="41d1d-300">Parameters provided for the method are not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-301"><span id="WBEM_E_SYSTEM_PROPERTY"></span><span id="wbem_e_system_property"></span>**\_Propriedade do \_ sistema WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-301"><span id="WBEM_E_SYSTEM_PROPERTY"></span><span id="wbem_e_system_property"></span>**WBEM\_E\_SYSTEM\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-302">2147749936 (0x80041030)</span><span class="sxs-lookup"><span data-stu-id="41d1d-302">2147749936 (0x80041030)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-303">Houve uma tentativa de obter qualificadores em uma propriedade do sistema.</span><span class="sxs-lookup"><span data-stu-id="41d1d-303">There was an attempt to get qualifiers on a system property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-304"><span id="WBEM_E_INVALID_PROPERTY"></span><span id="wbem_e_invalid_property"></span>**Propriedade de WBEM \_ E \_ inválida \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-304"><span id="WBEM_E_INVALID_PROPERTY"></span><span id="wbem_e_invalid_property"></span>**WBEM\_E\_INVALID\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-305">2147749937 (0x80041031)</span><span class="sxs-lookup"><span data-stu-id="41d1d-305">2147749937 (0x80041031)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-306">O tipo de propriedade não é reconhecido.</span><span class="sxs-lookup"><span data-stu-id="41d1d-306">Property type is not recognized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-307"><span id="WBEM_E_CALL_CANCELLED"></span><span id="wbem_e_call_cancelled"></span>**chamada de WBEM \_ E \_ \_ cancelada**</span><span class="sxs-lookup"><span data-stu-id="41d1d-307"><span id="WBEM_E_CALL_CANCELLED"></span><span id="wbem_e_call_cancelled"></span>**WBEM\_E\_CALL\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-308">2147749938 (0x80041032)</span><span class="sxs-lookup"><span data-stu-id="41d1d-308">2147749938 (0x80041032)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-309">O processo assíncrono foi cancelado internamente ou pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="41d1d-309">Asynchronous process has been canceled internally or by the user.</span></span> <span data-ttu-id="41d1d-310">Observe que, devido ao tempo e à natureza da operação assíncrona, a operação pode não ter sido realmente cancelada.</span><span class="sxs-lookup"><span data-stu-id="41d1d-310">Note that due to the timing and nature of the asynchronous operation, the operation may not have been truly canceled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-311"><span id="WBEM_E_SHUTTING_DOWN"></span><span id="wbem_e_shutting_down"></span>**WBEM \_ E \_ desligando \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-311"><span id="WBEM_E_SHUTTING_DOWN"></span><span id="wbem_e_shutting_down"></span>**WBEM\_E\_SHUTTING\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-312">2147749939 (0x80041033)</span><span class="sxs-lookup"><span data-stu-id="41d1d-312">2147749939 (0x80041033)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-313">O usuário solicitou uma operação enquanto o WMI está em processo de desligamento.</span><span class="sxs-lookup"><span data-stu-id="41d1d-313">User has requested an operation while WMI is in the process of shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-314"><span id="WBEM_E_PROPAGATED_METHOD"></span><span id="wbem_e_propagated_method"></span>**\_ \_ método propagado do WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-314"><span id="WBEM_E_PROPAGATED_METHOD"></span><span id="wbem_e_propagated_method"></span>**WBEM\_E\_PROPAGATED\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-315">2147749940 (0x80041034)</span><span class="sxs-lookup"><span data-stu-id="41d1d-315">2147749940 (0x80041034)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-316">Foi feita uma tentativa de reutilizar um nome de método existente de uma classe pai e as assinaturas não coincidem.</span><span class="sxs-lookup"><span data-stu-id="41d1d-316">Attempt was made to reuse an existing method name from a parent class and the signatures do not match.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-317"><span id="WBEM_E_UNSUPPORTED_PARAMETER"></span><span id="wbem_e_unsupported_parameter"></span>**parâmetro de WBEM \_ E \_ sem suporte \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-317"><span id="WBEM_E_UNSUPPORTED_PARAMETER"></span><span id="wbem_e_unsupported_parameter"></span>**WBEM\_E\_UNSUPPORTED\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-318">2147749941 (0x80041035)</span><span class="sxs-lookup"><span data-stu-id="41d1d-318">2147749941 (0x80041035)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-319">Um ou mais valores de parâmetro, como um texto de consulta, são muito complexos ou não têm suporte.</span><span class="sxs-lookup"><span data-stu-id="41d1d-319">One or more parameter values, such as a query text, is too complex or unsupported.</span></span> <span data-ttu-id="41d1d-320">Portanto, o WMI é solicitado a repetir a operação com parâmetros mais simples.</span><span class="sxs-lookup"><span data-stu-id="41d1d-320">WMI is therefore requested to retry the operation with simpler parameters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-321"><span id="WBEM_E_MISSING_PARAMETER_ID"></span><span id="wbem_e_missing_parameter_id"></span>**\_ID de \_ \_ parâmetro ausente \_ do WBEM E**</span><span class="sxs-lookup"><span data-stu-id="41d1d-321"><span id="WBEM_E_MISSING_PARAMETER_ID"></span><span id="wbem_e_missing_parameter_id"></span>**WBEM\_E\_MISSING\_PARAMETER\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-322">2147749942 (0x80041036)</span><span class="sxs-lookup"><span data-stu-id="41d1d-322">2147749942 (0x80041036)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-323">O parâmetro estava ausente da chamada do método.</span><span class="sxs-lookup"><span data-stu-id="41d1d-323">Parameter was missing from the method call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-324"><span id="WBEM_E_INVALID_PARAMETER_ID"></span><span id="wbem_e_invalid_parameter_id"></span>**ID de parâmetro de WBEM \_ E \_ inválido \_ \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-324"><span id="WBEM_E_INVALID_PARAMETER_ID"></span><span id="wbem_e_invalid_parameter_id"></span>**WBEM\_E\_INVALID\_PARAMETER\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-325">2147749943 (0x80041037)</span><span class="sxs-lookup"><span data-stu-id="41d1d-325">2147749943 (0x80041037)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-326">O parâmetro do método tem um qualificador de [**ID**](standard-wmi-qualifiers.md) que não é válido.</span><span class="sxs-lookup"><span data-stu-id="41d1d-326">Method parameter has an [**ID**](standard-wmi-qualifiers.md) qualifier that is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-327"><span id="WBEM_E_NONCONSECUTIVE_PARAMETER_IDS"></span><span id="wbem_e_nonconsecutive_parameter_ids"></span>**\_IDs de parâmetro WBEM E não \_ consecutivo \_ \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-327"><span id="WBEM_E_NONCONSECUTIVE_PARAMETER_IDS"></span><span id="wbem_e_nonconsecutive_parameter_ids"></span>**WBEM\_E\_NONCONSECUTIVE\_PARAMETER\_IDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-328">2147749944 (0x80041038)</span><span class="sxs-lookup"><span data-stu-id="41d1d-328">2147749944 (0x80041038)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-329">Um ou mais dos parâmetros de método têm qualificadores de [**ID**](standard-wmi-qualifiers.md) fora de sequência.</span><span class="sxs-lookup"><span data-stu-id="41d1d-329">One or more of the method parameters have [**ID**](standard-wmi-qualifiers.md) qualifiers that are out of sequence.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-330"><span id="WBEM_E_PARAMETER_ID_ON_RETVAL"></span><span id="wbem_e_parameter_id_on_retval"></span>**\_ \_ ID do parâmetro WBEM E \_ \_ no \_ RETVAL**</span><span class="sxs-lookup"><span data-stu-id="41d1d-330"><span id="WBEM_E_PARAMETER_ID_ON_RETVAL"></span><span id="wbem_e_parameter_id_on_retval"></span>**WBEM\_E\_PARAMETER\_ID\_ON\_RETVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-331">2147749945 (0x80041039)</span><span class="sxs-lookup"><span data-stu-id="41d1d-331">2147749945 (0x80041039)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-332">O valor de retorno para um método tem um qualificador de [**ID**](standard-wmi-qualifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="41d1d-332">Return value for a method has an [**ID**](standard-wmi-qualifiers.md) qualifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-333"><span id="WBEM_E_INVALID_OBJECT_PATH"></span><span id="wbem_e_invalid_object_path"></span>**caminho de objeto do WBEM \_ E \_ inválido \_ \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-333"><span id="WBEM_E_INVALID_OBJECT_PATH"></span><span id="wbem_e_invalid_object_path"></span>**WBEM\_E\_INVALID\_OBJECT\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-334">2147749946 (0x8004103A)</span><span class="sxs-lookup"><span data-stu-id="41d1d-334">2147749946 (0x8004103A)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-335">O caminho do objeto especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="41d1d-335">Specified object path was not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-336"><span id="WBEM_E_OUT_OF_DISK_SPACE"></span><span id="wbem_e_out_of_disk_space"></span>**WBEM \_ E \_ sem \_ \_ \_ espaço em disco**</span><span class="sxs-lookup"><span data-stu-id="41d1d-336"><span id="WBEM_E_OUT_OF_DISK_SPACE"></span><span id="wbem_e_out_of_disk_space"></span>**WBEM\_E\_OUT\_OF\_DISK\_SPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-337">2147749947 (0x8004103B)</span><span class="sxs-lookup"><span data-stu-id="41d1d-337">2147749947 (0x8004103B)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-338">O disco está sem espaço ou o limite de 4 GB no repositório do WMI (repositório CIM) foi atingido.</span><span class="sxs-lookup"><span data-stu-id="41d1d-338">Disk is out of space or the 4 GB limit on WMI repository (CIM repository) size is reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-339"><span id="WBEM_E_BUFFER_TOO_SMALL"></span><span id="wbem_e_buffer_too_small"></span>**o buffer do WBEM E o é \_ \_ \_ muito \_ pequeno**</span><span class="sxs-lookup"><span data-stu-id="41d1d-339"><span id="WBEM_E_BUFFER_TOO_SMALL"></span><span id="wbem_e_buffer_too_small"></span>**WBEM\_E\_BUFFER\_TOO\_SMALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-340">2147749948 (0x8004103C)</span><span class="sxs-lookup"><span data-stu-id="41d1d-340">2147749948 (0x8004103C)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-341">O buffer fornecido era muito pequeno para conter todos os objetos no enumerador ou para ler uma propriedade de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="41d1d-341">Supplied buffer was too small to hold all of the objects in the enumerator or to read a string property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-342"><span id="WBEM_E_UNSUPPORTED_PUT_EXTENSION"></span><span id="wbem_e_unsupported_put_extension"></span>**\_extensão de \_ Put E sem \_ suporte \_ do WBEM**</span><span class="sxs-lookup"><span data-stu-id="41d1d-342"><span id="WBEM_E_UNSUPPORTED_PUT_EXTENSION"></span><span id="wbem_e_unsupported_put_extension"></span>**WBEM\_E\_UNSUPPORTED\_PUT\_EXTENSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-343">2147749949 (0x8004103D)</span><span class="sxs-lookup"><span data-stu-id="41d1d-343">2147749949 (0x8004103D)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-344">O provedor não oferece suporte à operação Put solicitada.</span><span class="sxs-lookup"><span data-stu-id="41d1d-344">Provider does not support the requested put operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-345"><span id="WBEM_E_UNKNOWN_OBJECT_TYPE"></span><span id="wbem_e_unknown_object_type"></span>**\_tipo de objeto WBEM E \_ desconhecido \_ \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-345"><span id="WBEM_E_UNKNOWN_OBJECT_TYPE"></span><span id="wbem_e_unknown_object_type"></span>**WBEM\_E\_UNKNOWN\_OBJECT\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-346">2147749950 (0x8004103E)</span><span class="sxs-lookup"><span data-stu-id="41d1d-346">2147749950 (0x8004103E)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-347">O objeto com um tipo ou versão incorreto foi encontrado durante o marshaling.</span><span class="sxs-lookup"><span data-stu-id="41d1d-347">Object with an incorrect type or version was encountered during marshaling.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-348"><span id="WBEM_E_UNKNOWN_PACKET_TYPE"></span><span id="wbem_e_unknown_packet_type"></span>**\_tipo de pacote WBEM E \_ desconhecido \_ \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-348"><span id="WBEM_E_UNKNOWN_PACKET_TYPE"></span><span id="wbem_e_unknown_packet_type"></span>**WBEM\_E\_UNKNOWN\_PACKET\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-349">2147749951 (0x8004103F)</span><span class="sxs-lookup"><span data-stu-id="41d1d-349">2147749951 (0x8004103F)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-350">Um pacote com tipo ou versão incorreta foi encontrado durante o marshaling.</span><span class="sxs-lookup"><span data-stu-id="41d1d-350">Packet with an incorrect type or version was encountered during marshaling.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-351"><span id="WBEM_E_MARSHAL_VERSION_MISMATCH"></span><span id="wbem_e_marshal_version_mismatch"></span>**incompatibilidade de versão do WBEM \_ E \_ Marshal \_ \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-351"><span id="WBEM_E_MARSHAL_VERSION_MISMATCH"></span><span id="wbem_e_marshal_version_mismatch"></span>**WBEM\_E\_MARSHAL\_VERSION\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-352">2147749952 (0x80041040)</span><span class="sxs-lookup"><span data-stu-id="41d1d-352">2147749952 (0x80041040)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-353">O pacote tem uma versão sem suporte.</span><span class="sxs-lookup"><span data-stu-id="41d1d-353">Packet has an unsupported version.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-354"><span id="WBEM_E_MARSHAL_INVALID_SIGNATURE"></span><span id="wbem_e_marshal_invalid_signature"></span>**assinatura de WBEM \_ E \_ Marshal \_ inválido \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-354"><span id="WBEM_E_MARSHAL_INVALID_SIGNATURE"></span><span id="wbem_e_marshal_invalid_signature"></span>**WBEM\_E\_MARSHAL\_INVALID\_SIGNATURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-355">2147749953 (0x80041041)</span><span class="sxs-lookup"><span data-stu-id="41d1d-355">2147749953 (0x80041041)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-356">O pacote parece estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="41d1d-356">Packet appears to be corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-357"><span id="WBEM_E_INVALID_QUALIFIER"></span><span id="wbem_e_invalid_qualifier"></span>**\_qualificador do WBEM E \_ inválido \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-357"><span id="WBEM_E_INVALID_QUALIFIER"></span><span id="wbem_e_invalid_qualifier"></span>**WBEM\_E\_INVALID\_QUALIFIER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-358">2147749954 (0x80041042)</span><span class="sxs-lookup"><span data-stu-id="41d1d-358">2147749954 (0x80041042)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-359">Foi feita uma tentativa de qualificadores incompatíveis, como \[ colocar \] a chave em um objeto em vez de uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="41d1d-359">Attempt was made to mismatch qualifiers, such as putting \[key\] on an object instead of a property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-360"><span id="WBEM_E_INVALID_DUPLICATE_PARAMETER"></span><span id="wbem_e_invalid_duplicate_parameter"></span>**\_ \_ \_ parâmetro duplicado WBEM E inválido \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-360"><span id="WBEM_E_INVALID_DUPLICATE_PARAMETER"></span><span id="wbem_e_invalid_duplicate_parameter"></span>**WBEM\_E\_INVALID\_DUPLICATE\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-361">2147749955 (0x80041043)</span><span class="sxs-lookup"><span data-stu-id="41d1d-361">2147749955 (0x80041043)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-362">Parâmetro duplicado foi declarado em um método CIM.</span><span class="sxs-lookup"><span data-stu-id="41d1d-362">Duplicate parameter was declared in a CIM method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-363"><span id="WBEM_E_TOO_MUCH_DATA"></span><span id="wbem_e_too_much_data"></span>**WBEM \_ E \_ muito \_ \_ dados**</span><span class="sxs-lookup"><span data-stu-id="41d1d-363"><span id="WBEM_E_TOO_MUCH_DATA"></span><span id="wbem_e_too_much_data"></span>**WBEM\_E\_TOO\_MUCH\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-364">2147749956 (0x80041044)</span><span class="sxs-lookup"><span data-stu-id="41d1d-364">2147749956 (0x80041044)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-365">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="41d1d-365">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-366"><span id="WBEM_E_SERVER_TOO_BUSY"></span><span id="wbem_e_server_too_busy"></span>**WBEM \_ E \_ servidor \_ muito \_ ocupado**</span><span class="sxs-lookup"><span data-stu-id="41d1d-366"><span id="WBEM_E_SERVER_TOO_BUSY"></span><span id="wbem_e_server_too_busy"></span>**WBEM\_E\_SERVER\_TOO\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-367">2147749957 (0x80041045)</span><span class="sxs-lookup"><span data-stu-id="41d1d-367">2147749957 (0x80041045)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-368">Falha na chamada para [**IWbemObjectSink:: indication**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) .</span><span class="sxs-lookup"><span data-stu-id="41d1d-368">Call to [**IWbemObjectSink::Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) has failed.</span></span> <span data-ttu-id="41d1d-369">O provedor pode acionar o evento novamente.</span><span class="sxs-lookup"><span data-stu-id="41d1d-369">The provider can refire the event.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-370"><span id="WBEM_E_INVALID_FLAVOR"></span><span id="wbem_e_invalid_flavor"></span>**tipo de WBEM \_ E \_ inválido \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-370"><span id="WBEM_E_INVALID_FLAVOR"></span><span id="wbem_e_invalid_flavor"></span>**WBEM\_E\_INVALID\_FLAVOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-371">2147749958 (0x80041046)</span><span class="sxs-lookup"><span data-stu-id="41d1d-371">2147749958 (0x80041046)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-372">O tipo qualificador especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="41d1d-372">Specified qualifier flavor was not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-373"><span id="WBEM_E_CIRCULAR_REFERENCE"></span><span id="wbem_e_circular_reference"></span>**\_ \_ referência circular E de WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-373"><span id="WBEM_E_CIRCULAR_REFERENCE"></span><span id="wbem_e_circular_reference"></span>**WBEM\_E\_CIRCULAR\_REFERENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-374">2147749959 (0x80041047)</span><span class="sxs-lookup"><span data-stu-id="41d1d-374">2147749959 (0x80041047)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-375">Foi feita uma tentativa de criar uma referência que é circular (por exemplo, derivando uma classe a partir dela).</span><span class="sxs-lookup"><span data-stu-id="41d1d-375">Attempt was made to create a reference that is circular (for example, deriving a class from itself).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-376"><span id="WBEM_E_UNSUPPORTED_CLASS_UPDATE"></span><span id="wbem_e_unsupported_class_update"></span>**\_atualização de classe WBEM E \_ sem suporte \_ \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-376"><span id="WBEM_E_UNSUPPORTED_CLASS_UPDATE"></span><span id="wbem_e_unsupported_class_update"></span>**WBEM\_E\_UNSUPPORTED\_CLASS\_UPDATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-377">2147749960 (0x80041048)</span><span class="sxs-lookup"><span data-stu-id="41d1d-377">2147749960 (0x80041048)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-378">Não há suporte para a classe especificada.</span><span class="sxs-lookup"><span data-stu-id="41d1d-378">Specified class is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-379"><span id="WBEM_E_CANNOT_CHANGE_KEY_INHERITANCE"></span><span id="wbem_e_cannot_change_key_inheritance"></span>**WBEM \_ E \_ não pode \_ alterar a \_ herança de chave \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-379"><span id="WBEM_E_CANNOT_CHANGE_KEY_INHERITANCE"></span><span id="wbem_e_cannot_change_key_inheritance"></span>**WBEM\_E\_CANNOT\_CHANGE\_KEY\_INHERITANCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-380">2147749961 (0x80041049)</span><span class="sxs-lookup"><span data-stu-id="41d1d-380">2147749961 (0x80041049)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-381">Foi feita uma tentativa de alterar uma chave quando instâncias ou subclasses já estão usando a chave.</span><span class="sxs-lookup"><span data-stu-id="41d1d-381">Attempt was made to change a key when instances or subclasses are already using the key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-382"><span id="WBEM_E_CANNOT_CHANGE_INDEX_INHERITANCE"></span><span id="wbem_e_cannot_change_index_inheritance"></span>**WBEM \_ E \_ não é possível \_ alterar a \_ herança do índice \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-382"><span id="WBEM_E_CANNOT_CHANGE_INDEX_INHERITANCE"></span><span id="wbem_e_cannot_change_index_inheritance"></span>**WBEM\_E\_CANNOT\_CHANGE\_INDEX\_INHERITANCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-383">2147749968 (0x80041050)</span><span class="sxs-lookup"><span data-stu-id="41d1d-383">2147749968 (0x80041050)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-384">Foi feita uma tentativa de alterar um índice quando instâncias ou subclasses já estão usando o índice.</span><span class="sxs-lookup"><span data-stu-id="41d1d-384">An attempt was made to change an index when instances or subclasses are already using the index.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-385"><span id="WBEM_E_TOO_MANY_PROPERTIES"></span><span id="wbem_e_too_many_properties"></span>**WBEM \_ E \_ \_ muitas \_ Propriedades**</span><span class="sxs-lookup"><span data-stu-id="41d1d-385"><span id="WBEM_E_TOO_MANY_PROPERTIES"></span><span id="wbem_e_too_many_properties"></span>**WBEM\_E\_TOO\_MANY\_PROPERTIES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-386">2147749969 (0x80041051)</span><span class="sxs-lookup"><span data-stu-id="41d1d-386">2147749969 (0x80041051)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-387">Foi feita uma tentativa de criar mais propriedades do que a versão atual da classe dá suporte.</span><span class="sxs-lookup"><span data-stu-id="41d1d-387">Attempt was made to create more properties than the current version of the class supports.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-388"><span id="WBEM_E_UPDATE_TYPE_MISMATCH"></span><span id="wbem_e_update_type_mismatch"></span>**incompatibilidade de tipo de atualização WBEM \_ E \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-388"><span id="WBEM_E_UPDATE_TYPE_MISMATCH"></span><span id="wbem_e_update_type_mismatch"></span>**WBEM\_E\_UPDATE\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-389">2147749970 (0x80041052)</span><span class="sxs-lookup"><span data-stu-id="41d1d-389">2147749970 (0x80041052)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-390">A propriedade foi redefinida com um tipo conflitante em uma classe derivada.</span><span class="sxs-lookup"><span data-stu-id="41d1d-390">Property was redefined with a conflicting type in a derived class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-391"><span id="WBEM_E_UPDATE_OVERRIDE_NOT_ALLOWED"></span><span id="wbem_e_update_override_not_allowed"></span>**substituição de atualização de WBEM \_ E \_ \_ \_ não \_ permitida**</span><span class="sxs-lookup"><span data-stu-id="41d1d-391"><span id="WBEM_E_UPDATE_OVERRIDE_NOT_ALLOWED"></span><span id="wbem_e_update_override_not_allowed"></span>**WBEM\_E\_UPDATE\_OVERRIDE\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-392">2147749971 (0x80041053)</span><span class="sxs-lookup"><span data-stu-id="41d1d-392">2147749971 (0x80041053)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-393">Foi feita uma tentativa em uma classe derivada para substituir um qualificador que não pode ser substituído.</span><span class="sxs-lookup"><span data-stu-id="41d1d-393">Attempt was made in a derived class to override a qualifier that cannot be overridden.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-394"><span id="WBEM_E_UPDATE_PROPAGATED_METHOD"></span><span id="wbem_e_update_propagated_method"></span>**\_ \_ \_ método propagado de atualização de WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-394"><span id="WBEM_E_UPDATE_PROPAGATED_METHOD"></span><span id="wbem_e_update_propagated_method"></span>**WBEM\_E\_UPDATE\_PROPAGATED\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-395">2147749972 (0x80041054)</span><span class="sxs-lookup"><span data-stu-id="41d1d-395">2147749972 (0x80041054)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-396">O método foi declarado novamente com uma assinatura conflitante em uma classe derivada.</span><span class="sxs-lookup"><span data-stu-id="41d1d-396">Method was re-declared with a conflicting signature in a derived class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-397"><span id="WBEM_E_METHOD_NOT_IMPLEMENTED"></span><span id="wbem_e_method_not_implemented"></span>**\_método WBEM \_ E \_ não \_ implementado**</span><span class="sxs-lookup"><span data-stu-id="41d1d-397"><span id="WBEM_E_METHOD_NOT_IMPLEMENTED"></span><span id="wbem_e_method_not_implemented"></span>**WBEM\_E\_METHOD\_NOT\_IMPLEMENTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-398">2147749973 (0x80041055)</span><span class="sxs-lookup"><span data-stu-id="41d1d-398">2147749973 (0x80041055)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-399">Foi feita uma tentativa de executar um método não marcado com \[ implementado \] em nenhuma classe relevante.</span><span class="sxs-lookup"><span data-stu-id="41d1d-399">Attempt was made to execute a method not marked with \[implemented\] in any relevant class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-400"><span id="WBEM_E_METHOD_DISABLED"></span><span id="wbem_e_method_disabled"></span>**\_método WBEM \_ E \_ desabilitado**</span><span class="sxs-lookup"><span data-stu-id="41d1d-400"><span id="WBEM_E_METHOD_DISABLED"></span><span id="wbem_e_method_disabled"></span>**WBEM\_E\_METHOD\_DISABLED**</span></span>
</dt> <dd> <dl> <span data-ttu-id="41d1d-401"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="41d1d-401"><dt>


</dt> <dt></span></span>



<span data-ttu-id="41d1d-402">Foi feita uma tentativa de executar um método marcado com \[ desabilitado \] .</span><span class="sxs-lookup"><span data-stu-id="41d1d-402">Attempt was made to execute a method marked with \[disabled\].</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-403"><span id="WBEM_E_REFRESHER_BUSY"></span><span id="wbem_e_refresher_busy"></span>**\_ \_ atualizador de WBEM E \_ ocupado**</span><span class="sxs-lookup"><span data-stu-id="41d1d-403"><span id="WBEM_E_REFRESHER_BUSY"></span><span id="wbem_e_refresher_busy"></span>**WBEM\_E\_REFRESHER\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-404">2147749975 (0x80041057)</span><span class="sxs-lookup"><span data-stu-id="41d1d-404">2147749975 (0x80041057)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-405">O atualizador está ocupado com outra operação.</span><span class="sxs-lookup"><span data-stu-id="41d1d-405">Refresher is busy with another operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-406"><span id="WBEM_E_UNPARSABLE_QUERY"></span><span id="wbem_e_unparsable_query"></span>**\_consulta WBEM E não \_ analisável \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-406"><span id="WBEM_E_UNPARSABLE_QUERY"></span><span id="wbem_e_unparsable_query"></span>**WBEM\_E\_UNPARSABLE\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-407">2147749976 (0x80041058)</span><span class="sxs-lookup"><span data-stu-id="41d1d-407">2147749976 (0x80041058)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-408">A consulta de filtragem é sintaticamente inválida.</span><span class="sxs-lookup"><span data-stu-id="41d1d-408">Filtering query is syntactically not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-409"><span id="WBEM_E_NOT_EVENT_CLASS"></span><span id="wbem_e_not_event_class"></span>**\_classe de evento WBEM E \_ not \_ \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-409"><span id="WBEM_E_NOT_EVENT_CLASS"></span><span id="wbem_e_not_event_class"></span>**WBEM\_E\_NOT\_EVENT\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-410">2147749977 (0x80041059)</span><span class="sxs-lookup"><span data-stu-id="41d1d-410">2147749977 (0x80041059)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-411">A cláusula FROM de uma consulta de filtragem faz referência a uma classe que não é uma classe de evento (não derivada do [**\_ \_ evento**](--event.md)).</span><span class="sxs-lookup"><span data-stu-id="41d1d-411">The FROM clause of a filtering query references a class that is not an event class (not derived from [**\_\_Event**](--event.md)).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-412"><span id="WBEM_E_MISSING_GROUP_WITHIN"></span><span id="wbem_e_missing_group_within"></span>**WBEM \_ E \_ faltando \_ grupo \_ dentro de**</span><span class="sxs-lookup"><span data-stu-id="41d1d-412"><span id="WBEM_E_MISSING_GROUP_WITHIN"></span><span id="wbem_e_missing_group_within"></span>**WBEM\_E\_MISSING\_GROUP\_WITHIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-413">2147749978 (0x8004105A)</span><span class="sxs-lookup"><span data-stu-id="41d1d-413">2147749978 (0x8004105A)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-414">Uma cláusula GROUP BY foi usada sem a cláusula GROUP WITHIN correspondente.</span><span class="sxs-lookup"><span data-stu-id="41d1d-414">A GROUP BY clause was used without the corresponding GROUP WITHIN clause.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-415"><span id="WBEM_E_MISSING_AGGREGATION_LIST"></span><span id="wbem_e_missing_aggregation_list"></span>**WBEM \_ E \_ \_ lista de agregação ausente \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-415"><span id="WBEM_E_MISSING_AGGREGATION_LIST"></span><span id="wbem_e_missing_aggregation_list"></span>**WBEM\_E\_MISSING\_AGGREGATION\_LIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-416">2147749979 (0x8004105B)</span><span class="sxs-lookup"><span data-stu-id="41d1d-416">2147749979 (0x8004105B)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-417">Uma cláusula GROUP BY foi usada.</span><span class="sxs-lookup"><span data-stu-id="41d1d-417">A GROUP BY clause was used.</span></span> <span data-ttu-id="41d1d-418">Não há suporte para a agregação em todas as propriedades.</span><span class="sxs-lookup"><span data-stu-id="41d1d-418">Aggregation on all properties is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-419"><span id="WBEM_E_PROPERTY_NOT_AN_OBJECT"></span><span id="wbem_e_property_not_an_object"></span>**\_ \_ a propriedade WBEM E \_ não \_ um \_ objeto**</span><span class="sxs-lookup"><span data-stu-id="41d1d-419"><span id="WBEM_E_PROPERTY_NOT_AN_OBJECT"></span><span id="wbem_e_property_not_an_object"></span>**WBEM\_E\_PROPERTY\_NOT\_AN\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-420">2147749980 (0x8004105C)</span><span class="sxs-lookup"><span data-stu-id="41d1d-420">2147749980 (0x8004105C)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-421">A notação de ponto foi usada em uma propriedade que não é um objeto inserido.</span><span class="sxs-lookup"><span data-stu-id="41d1d-421">Dot notation was used on a property that is not an embedded object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-422"><span id="WBEM_E_AGGREGATING_BY_OBJECT"></span><span id="wbem_e_aggregating_by_object"></span>**WBEM \_ E \_ agregando \_ por \_ objeto**</span><span class="sxs-lookup"><span data-stu-id="41d1d-422"><span id="WBEM_E_AGGREGATING_BY_OBJECT"></span><span id="wbem_e_aggregating_by_object"></span>**WBEM\_E\_AGGREGATING\_BY\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-423">2147749981 (0x8004105D)</span><span class="sxs-lookup"><span data-stu-id="41d1d-423">2147749981 (0x8004105D)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-424">Uma cláusula GROUP BY faz referência a uma propriedade que é um objeto inserido sem usar a notação de ponto.</span><span class="sxs-lookup"><span data-stu-id="41d1d-424">A GROUP BY clause references a property that is an embedded object without using dot notation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-425"><span id="WBEM_E_UNINTERPRETABLE_PROVIDER_QUERY"></span><span id="wbem_e_uninterpretable_provider_query"></span>**\_consulta de provedor WBEM E não \_ interpretável \_ \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-425"><span id="WBEM_E_UNINTERPRETABLE_PROVIDER_QUERY"></span><span id="wbem_e_uninterpretable_provider_query"></span>**WBEM\_E\_UNINTERPRETABLE\_PROVIDER\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-426">2147749983 (0x8004105F)</span><span class="sxs-lookup"><span data-stu-id="41d1d-426">2147749983 (0x8004105F)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-427">A consulta de registro do provedor de eventos ([**\_ \_ EventProviderRegistration**](--eventproviderregistration.md)) não especificou as classes para as quais os eventos foram fornecidos.</span><span class="sxs-lookup"><span data-stu-id="41d1d-427">Event provider registration query ([**\_\_EventProviderRegistration**](--eventproviderregistration.md)) did not specify the classes for which events were provided.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-428"><span id="WBEM_E_BACKUP_RESTORE_WINMGMT_RUNNING"></span><span id="wbem_e_backup_restore_winmgmt_running"></span>**\_execução da \_ \_ restauração de \_ backup \_ do WBEM E**</span><span class="sxs-lookup"><span data-stu-id="41d1d-428"><span id="WBEM_E_BACKUP_RESTORE_WINMGMT_RUNNING"></span><span id="wbem_e_backup_restore_winmgmt_running"></span>**WBEM\_E\_BACKUP\_RESTORE\_WINMGMT\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-429">2147749984 (0x80041060)</span><span class="sxs-lookup"><span data-stu-id="41d1d-429">2147749984 (0x80041060)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-430">Foi feita uma solicitação para fazer backup ou restaurar o repositório enquanto ele estava em uso pelo WinMgmt.exe ou pelo processo SVCHOST que contém o serviço WMI.</span><span class="sxs-lookup"><span data-stu-id="41d1d-430">Request was made to back up or restore the repository while it was in use by WinMgmt.exe, or by the SVCHOST process that contains the WMI service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-431"><span id="WBEM_E_QUEUE_OVERFLOW"></span><span id="wbem_e_queue_overflow"></span>**\_estouro de \_ fila WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-431"><span id="WBEM_E_QUEUE_OVERFLOW"></span><span id="wbem_e_queue_overflow"></span>**WBEM\_E\_QUEUE\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-432">2147749985 (0x80041061)</span><span class="sxs-lookup"><span data-stu-id="41d1d-432">2147749985 (0x80041061)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-433">A fila de entrega assíncrona estourou do consumidor de eventos está muito lenta.</span><span class="sxs-lookup"><span data-stu-id="41d1d-433">Asynchronous delivery queue overflowed from the event consumer being too slow.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-434"><span id="WBEM_E_PRIVILEGE_NOT_HELD"></span><span id="wbem_e_privilege_not_held"></span>**WBEM \_ E \_ privilégio \_ não \_ mantidos**</span><span class="sxs-lookup"><span data-stu-id="41d1d-434"><span id="WBEM_E_PRIVILEGE_NOT_HELD"></span><span id="wbem_e_privilege_not_held"></span>**WBEM\_E\_PRIVILEGE\_NOT\_HELD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-435">2147749986 (0x80041062)</span><span class="sxs-lookup"><span data-stu-id="41d1d-435">2147749986 (0x80041062)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-436">Falha na operação porque o cliente não tinha o privilégio de segurança necessário.</span><span class="sxs-lookup"><span data-stu-id="41d1d-436">Operation failed because the client did not have the necessary security privilege.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-437"><span id="WBEM_E_INVALID_OPERATOR"></span><span id="wbem_e_invalid_operator"></span>**\_ \_ operador inválido do WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-437"><span id="WBEM_E_INVALID_OPERATOR"></span><span id="wbem_e_invalid_operator"></span>**WBEM\_E\_INVALID\_OPERATOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-438">2147749987 (0x80041063)</span><span class="sxs-lookup"><span data-stu-id="41d1d-438">2147749987 (0x80041063)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-439">O operador não é válido para este tipo de propriedade.</span><span class="sxs-lookup"><span data-stu-id="41d1d-439">Operator is not valid for this property type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-440"><span id="WBEM_E_LOCAL_CREDENTIALS"></span><span id="wbem_e_local_credentials"></span>**\_ \_ credenciais locais do WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-440"><span id="WBEM_E_LOCAL_CREDENTIALS"></span><span id="wbem_e_local_credentials"></span>**WBEM\_E\_LOCAL\_CREDENTIALS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-441">2147749988 (0x80041064)</span><span class="sxs-lookup"><span data-stu-id="41d1d-441">2147749988 (0x80041064)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-442">O usuário especificou nome de usuário/senha/autoridade em uma conexão local.</span><span class="sxs-lookup"><span data-stu-id="41d1d-442">User specified a username/password/authority on a local connection.</span></span> <span data-ttu-id="41d1d-443">O usuário deve usar um nome de usuário/senha em branco e contar com a segurança padrão.</span><span class="sxs-lookup"><span data-stu-id="41d1d-443">The user must use a blank username/password and rely on default security.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-444"><span id="WBEM_E_CANNOT_BE_ABSTRACT"></span><span id="wbem_e_cannot_be_abstract"></span>**WBEM \_ E \_ não podem \_ ser \_ abstratos**</span><span class="sxs-lookup"><span data-stu-id="41d1d-444"><span id="WBEM_E_CANNOT_BE_ABSTRACT"></span><span id="wbem_e_cannot_be_abstract"></span>**WBEM\_E\_CANNOT\_BE\_ABSTRACT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-445">2147749989 (0x80041065)</span><span class="sxs-lookup"><span data-stu-id="41d1d-445">2147749989 (0x80041065)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-446">A classe tornou-se abstrata quando sua classe pai não é abstrata.</span><span class="sxs-lookup"><span data-stu-id="41d1d-446">Class was made abstract when its parent class is not abstract.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-447"><span id="WBEM_E_AMENDED_OBJECT"></span><span id="wbem_e_amended_object"></span>**\_objeto de \_ emendado E de WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-447"><span id="WBEM_E_AMENDED_OBJECT"></span><span id="wbem_e_amended_object"></span>**WBEM\_E\_AMENDED\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-448">2147749990 (0x80041066)</span><span class="sxs-lookup"><span data-stu-id="41d1d-448">2147749990 (0x80041066)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-449">O objeto emendado foi gravado sem o **sinalizador WBEM usar sinalizador de \_ \_ \_ \_ qualificadores corrigidos** sendo especificado.</span><span class="sxs-lookup"><span data-stu-id="41d1d-449">Amended object was written without the **WBEM\_FLAG\_USE\_AMENDED\_QUALIFIERS** flag being specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-450"><span id="WBEM_E_CLIENT_TOO_SLOW"></span><span id="wbem_e_client_too_slow"></span>**\_cliente WBEM E/s \_ \_ muito \_ lento**</span><span class="sxs-lookup"><span data-stu-id="41d1d-450"><span id="WBEM_E_CLIENT_TOO_SLOW"></span><span id="wbem_e_client_too_slow"></span>**WBEM\_E\_CLIENT\_TOO\_SLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-451">2147749991 (0x80041067)</span><span class="sxs-lookup"><span data-stu-id="41d1d-451">2147749991 (0x80041067)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-452">O cliente não recuperou objetos com rapidez suficiente a partir de uma enumeração.</span><span class="sxs-lookup"><span data-stu-id="41d1d-452">Client did not retrieve objects quickly enough from an enumeration.</span></span> <span data-ttu-id="41d1d-453">Essa constante é retornada quando um cliente cria um objeto de enumeração, mas não recupera objetos do enumerador em tempo hábil, fazendo com que os caches do objeto do enumerador sejam armazenados em backup.</span><span class="sxs-lookup"><span data-stu-id="41d1d-453">This constant is returned when a client creates an enumeration object, but does not retrieve objects from the enumerator in a timely fashion, causing the enumerator's object caches to back up.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-454"><span id="WBEM_E_NULL_SECURITY_DESCRIPTOR"></span><span id="wbem_e_null_security_descriptor"></span>**\_ \_ \_ descritor de segurança de WBEM E nulo \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-454"><span id="WBEM_E_NULL_SECURITY_DESCRIPTOR"></span><span id="wbem_e_null_security_descriptor"></span>**WBEM\_E\_NULL\_SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-455">2147749992 (0x80041068)</span><span class="sxs-lookup"><span data-stu-id="41d1d-455">2147749992 (0x80041068)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-456">Foi usado um descritor de segurança nulo.</span><span class="sxs-lookup"><span data-stu-id="41d1d-456">Null security descriptor was used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-457"><span id="WBEM_E_TIMED_OUT"></span><span id="wbem_e_timed_out"></span>**WBEM \_ E \_ atingiu o tempo \_ limite**</span><span class="sxs-lookup"><span data-stu-id="41d1d-457"><span id="WBEM_E_TIMED_OUT"></span><span id="wbem_e_timed_out"></span>**WBEM\_E\_TIMED\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-458">2147749993 (0x80041069)</span><span class="sxs-lookup"><span data-stu-id="41d1d-458">2147749993 (0x80041069)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-459">Tempo limite da operação atingido.</span><span class="sxs-lookup"><span data-stu-id="41d1d-459">Operation timed out.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-460"><span id="WBEM_E_INVALID_ASSOCIATION"></span><span id="wbem_e_invalid_association"></span>**Associação de WBEM \_ E \_ inválida \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-460"><span id="WBEM_E_INVALID_ASSOCIATION"></span><span id="wbem_e_invalid_association"></span>**WBEM\_E\_INVALID\_ASSOCIATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-461">2147749994</span><span class="sxs-lookup"><span data-stu-id="41d1d-461">2147749994</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-462">A associação não é válida.</span><span class="sxs-lookup"><span data-stu-id="41d1d-462">Association is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-463"><span id="WBEM_E_AMBIGUOUS_OPERATION"></span><span id="wbem_e_ambiguous_operation"></span>**operação de WBEM \_ E \_ ambígua \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-463"><span id="WBEM_E_AMBIGUOUS_OPERATION"></span><span id="wbem_e_ambiguous_operation"></span>**WBEM\_E\_AMBIGUOUS\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-464">2147749995 (0x8004106B)</span><span class="sxs-lookup"><span data-stu-id="41d1d-464">2147749995 (0x8004106B)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-465">A operação era ambígua.</span><span class="sxs-lookup"><span data-stu-id="41d1d-465">Operation was ambiguous.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-466"><span id="WBEM_E_QUOTA_VIOLATION"></span><span id="wbem_e_quota_violation"></span>**\_violação de \_ cota \_ E de WBEM**</span><span class="sxs-lookup"><span data-stu-id="41d1d-466"><span id="WBEM_E_QUOTA_VIOLATION"></span><span id="wbem_e_quota_violation"></span>**WBEM\_E\_QUOTA\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-467">2147749996 (0x8004106C)</span><span class="sxs-lookup"><span data-stu-id="41d1d-467">2147749996 (0x8004106C)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-468">O WMI está ocupando muita memória.</span><span class="sxs-lookup"><span data-stu-id="41d1d-468">WMI is taking up too much memory.</span></span> <span data-ttu-id="41d1d-469">Isso pode ser causado por baixa disponibilidade de memória ou consumo excessivo de memória pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="41d1d-469">This can be caused by low memory availability or excessive memory consumption by WMI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-470"><span id="WBEM_E_TRANSACTION_CONFLICT"></span><span id="wbem_e_transaction_conflict"></span>**\_conflito de \_ Transações WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-470"><span id="WBEM_E_TRANSACTION_CONFLICT"></span><span id="wbem_e_transaction_conflict"></span>**WBEM\_E\_TRANSACTION\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-471">2147749997 (0x8004106D)</span><span class="sxs-lookup"><span data-stu-id="41d1d-471">2147749997 (0x8004106D)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-472">A operação resultou em um conflito de transação.</span><span class="sxs-lookup"><span data-stu-id="41d1d-472">Operation resulted in a transaction conflict.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-473"><span id="WBEM_E_FORCED_ROLLBACK"></span><span id="wbem_e_forced_rollback"></span>**reversão do WBEM \_ E \_ forçada \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-473"><span id="WBEM_E_FORCED_ROLLBACK"></span><span id="wbem_e_forced_rollback"></span>**WBEM\_E\_FORCED\_ROLLBACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-474">2147749998 (0x8004106E)</span><span class="sxs-lookup"><span data-stu-id="41d1d-474">2147749998 (0x8004106E)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-475">A transação forçou uma reversão.</span><span class="sxs-lookup"><span data-stu-id="41d1d-475">Transaction forced a rollback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-476"><span id="WBEM_E_UNSUPPORTED_LOCALE"></span><span id="wbem_e_unsupported_locale"></span>**localidade do WBEM \_ E \_ sem suporte \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-476"><span id="WBEM_E_UNSUPPORTED_LOCALE"></span><span id="wbem_e_unsupported_locale"></span>**WBEM\_E\_UNSUPPORTED\_LOCALE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-477">2147749999 (0x8004106F)</span><span class="sxs-lookup"><span data-stu-id="41d1d-477">2147749999 (0x8004106F)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-478">Não há suporte para a localidade usada na chamada.</span><span class="sxs-lookup"><span data-stu-id="41d1d-478">Locale used in the call is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-479"><span id="WBEM_E_HANDLE_OUT_OF_DATE"></span><span id="wbem_e_handle_out_of_date"></span>**\_ \_ identificador de WBEM E \_ desatualizado \_ \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-479"><span id="WBEM_E_HANDLE_OUT_OF_DATE"></span><span id="wbem_e_handle_out_of_date"></span>**WBEM\_E\_HANDLE\_OUT\_OF\_DATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-480">2147750000 (0x80041070)</span><span class="sxs-lookup"><span data-stu-id="41d1d-480">2147750000 (0x80041070)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-481">O identificador de objeto está desatualizado.</span><span class="sxs-lookup"><span data-stu-id="41d1d-481">Object handle is out-of-date.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-482"><span id="WBEM_E_CONNECTION_FAILED"></span><span id="wbem_e_connection_failed"></span>**\_ \_ falha na conexão do WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-482"><span id="WBEM_E_CONNECTION_FAILED"></span><span id="wbem_e_connection_failed"></span>**WBEM\_E\_CONNECTION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-483">2147750001 (0x80041071)</span><span class="sxs-lookup"><span data-stu-id="41d1d-483">2147750001 (0x80041071)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-484">Falha na conexão com o banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="41d1d-484">Connection to the SQL database failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-485"><span id="WBEM_E_INVALID_HANDLE_REQUEST"></span><span id="wbem_e_invalid_handle_request"></span>**\_solicitação de \_ \_ identificador inválido \_ do WBEM E**</span><span class="sxs-lookup"><span data-stu-id="41d1d-485"><span id="WBEM_E_INVALID_HANDLE_REQUEST"></span><span id="wbem_e_invalid_handle_request"></span>**WBEM\_E\_INVALID\_HANDLE\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-486">2147750002 (0x80041072)</span><span class="sxs-lookup"><span data-stu-id="41d1d-486">2147750002 (0x80041072)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-487">A solicitação de identificador não era válida.</span><span class="sxs-lookup"><span data-stu-id="41d1d-487">Handle request was not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-488"><span id="WBEM_E_PROPERTY_NAME_TOO_WIDE"></span><span id="wbem_e_property_name_too_wide"></span>**\_nome da propriedade WBEM E \_ \_ \_ muito \_ grande**</span><span class="sxs-lookup"><span data-stu-id="41d1d-488"><span id="WBEM_E_PROPERTY_NAME_TOO_WIDE"></span><span id="wbem_e_property_name_too_wide"></span>**WBEM\_E\_PROPERTY\_NAME\_TOO\_WIDE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-489">2147750003 (0x80041073)</span><span class="sxs-lookup"><span data-stu-id="41d1d-489">2147750003 (0x80041073)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-490">O nome da propriedade contém mais de 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="41d1d-490">Property name contains more than 255 characters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-491"><span id="WBEM_E_CLASS_NAME_TOO_WIDE"></span><span id="wbem_e_class_name_too_wide"></span>**\_nome de classe WBEM E \_ \_ \_ muito \_ grande**</span><span class="sxs-lookup"><span data-stu-id="41d1d-491"><span id="WBEM_E_CLASS_NAME_TOO_WIDE"></span><span id="wbem_e_class_name_too_wide"></span>**WBEM\_E\_CLASS\_NAME\_TOO\_WIDE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-492">2147750004 (0x80041074)</span><span class="sxs-lookup"><span data-stu-id="41d1d-492">2147750004 (0x80041074)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-493">O nome da classe contém mais de 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="41d1d-493">Class name contains more than 255 characters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-494"><span id="WBEM_E_METHOD_NAME_TOO_WIDE"></span><span id="wbem_e_method_name_too_wide"></span>**\_nome do método WBEM E \_ \_ \_ muito \_ grande**</span><span class="sxs-lookup"><span data-stu-id="41d1d-494"><span id="WBEM_E_METHOD_NAME_TOO_WIDE"></span><span id="wbem_e_method_name_too_wide"></span>**WBEM\_E\_METHOD\_NAME\_TOO\_WIDE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-495">2147750005 (0x80041075)</span><span class="sxs-lookup"><span data-stu-id="41d1d-495">2147750005 (0x80041075)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-496">O nome do método contém mais de 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="41d1d-496">Method name contains more than 255 characters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-497"><span id="WBEM_E_QUALIFIER_NAME_TOO_WIDE"></span><span id="wbem_e_qualifier_name_too_wide"></span>**o \_ nome do qualificador E do WBEM é \_ \_ \_ muito \_ grande**</span><span class="sxs-lookup"><span data-stu-id="41d1d-497"><span id="WBEM_E_QUALIFIER_NAME_TOO_WIDE"></span><span id="wbem_e_qualifier_name_too_wide"></span>**WBEM\_E\_QUALIFIER\_NAME\_TOO\_WIDE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-498">2147750006 (0x80041076)</span><span class="sxs-lookup"><span data-stu-id="41d1d-498">2147750006 (0x80041076)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-499">O nome do qualificador contém mais de 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="41d1d-499">Qualifier name contains more than 255 characters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-500"><span id="WBEM_E_RERUN_COMMAND"></span><span id="wbem_e_rerun_command"></span>**WBEM \_ E \_ executar novamente o \_ comando**</span><span class="sxs-lookup"><span data-stu-id="41d1d-500"><span id="WBEM_E_RERUN_COMMAND"></span><span id="wbem_e_rerun_command"></span>**WBEM\_E\_RERUN\_COMMAND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-501">2147750007 (0x80041077)</span><span class="sxs-lookup"><span data-stu-id="41d1d-501">2147750007 (0x80041077)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-502">O comando SQL deve ser executado novamente porque há um deadlock no SQL.</span><span class="sxs-lookup"><span data-stu-id="41d1d-502">The SQL command must be rerun because there is a deadlock in SQL.</span></span> <span data-ttu-id="41d1d-503">Isso pode ser retornado somente quando os dados estão sendo armazenados em um banco de dado SQL.</span><span class="sxs-lookup"><span data-stu-id="41d1d-503">This can be returned only when data is being stored in an SQL database.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-504"><span id="WBEM_E_DATABASE_VER_MISMATCH"></span><span id="wbem_e_database_ver_mismatch"></span>**incompatibilidade de \_ versão do banco de dados WBEM E \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-504"><span id="WBEM_E_DATABASE_VER_MISMATCH"></span><span id="wbem_e_database_ver_mismatch"></span>**WBEM\_E\_DATABASE\_VER\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-505">2147750008 (0x80041078)</span><span class="sxs-lookup"><span data-stu-id="41d1d-505">2147750008 (0x80041078)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-506">A versão do banco de dados não corresponde à versão que o driver do repositório processa.</span><span class="sxs-lookup"><span data-stu-id="41d1d-506">The database version does not match the version that the repository driver processes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-507"><span id="WBEM_E_VETO_DELETE"></span><span id="wbem_e_veto_delete"></span>**exclusão de WBEM \_ E \_ veta \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-507"><span id="WBEM_E_VETO_DELETE"></span><span id="wbem_e_veto_delete"></span>**WBEM\_E\_VETO\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-508">2147750009 (0x80041079)</span><span class="sxs-lookup"><span data-stu-id="41d1d-508">2147750009 (0x80041079)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-509">O WMI não pode executar a operação de exclusão porque o provedor não permite.</span><span class="sxs-lookup"><span data-stu-id="41d1d-509">WMI cannot execute the delete operation because the provider does not allow it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-510"><span id="WBEM_E_VETO_PUT"></span><span id="wbem_e_veto_put"></span>**WBEM \_ E \_ vetar \_ put**</span><span class="sxs-lookup"><span data-stu-id="41d1d-510"><span id="WBEM_E_VETO_PUT"></span><span id="wbem_e_veto_put"></span>**WBEM\_E\_VETO\_PUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-511">2147750010 (0x8004107A)</span><span class="sxs-lookup"><span data-stu-id="41d1d-511">2147750010 (0x8004107A)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-512">O WMI não pode executar a operação Put porque o provedor não permite.</span><span class="sxs-lookup"><span data-stu-id="41d1d-512">WMI cannot execute the put operation because the provider does not allow it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-513"><span id="WBEM_E_INVALID_LOCALE"></span><span id="wbem_e_invalid_locale"></span>**\_ \_ localidade inválida do WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-513"><span id="WBEM_E_INVALID_LOCALE"></span><span id="wbem_e_invalid_locale"></span>**WBEM\_E\_INVALID\_LOCALE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-514">2147750016 (0x80041080)</span><span class="sxs-lookup"><span data-stu-id="41d1d-514">2147750016 (0x80041080)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-515">O identificador de localidade especificado não era válido para a operação.</span><span class="sxs-lookup"><span data-stu-id="41d1d-515">Specified locale identifier was not valid for the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-516"><span id="WBEM_E_PROVIDER_SUSPENDED"></span><span id="wbem_e_provider_suspended"></span>**\_provedor WBEM \_ E \_ suspenso**</span><span class="sxs-lookup"><span data-stu-id="41d1d-516"><span id="WBEM_E_PROVIDER_SUSPENDED"></span><span id="wbem_e_provider_suspended"></span>**WBEM\_E\_PROVIDER\_SUSPENDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-517">2147750017 (0x80041081)</span><span class="sxs-lookup"><span data-stu-id="41d1d-517">2147750017 (0x80041081)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-518">O provedor está suspenso.</span><span class="sxs-lookup"><span data-stu-id="41d1d-518">Provider is suspended.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-519"><span id="WBEM_E_SYNCHRONIZATION_REQUIRED"></span><span id="wbem_e_synchronization_required"></span>**sincronização de WBEM \_ E \_ \_ necessária**</span><span class="sxs-lookup"><span data-stu-id="41d1d-519"><span id="WBEM_E_SYNCHRONIZATION_REQUIRED"></span><span id="wbem_e_synchronization_required"></span>**WBEM\_E\_SYNCHRONIZATION\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-520">2147750018 (0x80041082)</span><span class="sxs-lookup"><span data-stu-id="41d1d-520">2147750018 (0x80041082)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-521">O objeto deve ser gravado no repositório WMI e recuperado novamente para que a operação solicitada possa ser realizada com sucesso.</span><span class="sxs-lookup"><span data-stu-id="41d1d-521">Object must be written to the WMI repository and retrieved again before the requested operation can succeed.</span></span> <span data-ttu-id="41d1d-522">Essa constante é retornada quando um objeto deve ser confirmado e recuperado para ver o valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="41d1d-522">This constant is returned when an object must be committed and retrieved to see the property value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-523"><span id="WBEM_E_NO_SCHEMA"></span><span id="wbem_e_no_schema"></span>**WBEM \_ E \_ sem \_ esquema**</span><span class="sxs-lookup"><span data-stu-id="41d1d-523"><span id="WBEM_E_NO_SCHEMA"></span><span id="wbem_e_no_schema"></span>**WBEM\_E\_NO\_SCHEMA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-524">2147750019 (0x80041083)</span><span class="sxs-lookup"><span data-stu-id="41d1d-524">2147750019 (0x80041083)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-525">A operação não pode ser concluída; nenhum esquema está disponível.</span><span class="sxs-lookup"><span data-stu-id="41d1d-525">Operation cannot be completed; no schema is available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-526"><span id="WBEM_E_PROVIDER_ALREADY_REGISTERED"></span><span id="wbem_e_provider_already_registered"></span>**\_provedor WBEM \_ E \_ já \_ registrado**</span><span class="sxs-lookup"><span data-stu-id="41d1d-526"><span id="WBEM_E_PROVIDER_ALREADY_REGISTERED"></span><span id="wbem_e_provider_already_registered"></span>**WBEM\_E\_PROVIDER\_ALREADY\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-527">02147750020 (0x119FD010)</span><span class="sxs-lookup"><span data-stu-id="41d1d-527">02147750020 (0x119FD010)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-528">O provedor não pode ser registrado porque já está registrado.</span><span class="sxs-lookup"><span data-stu-id="41d1d-528">Provider cannot be registered because it is already registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-529"><span id="WBEM_E_PROVIDER_NOT_REGISTERED"></span><span id="wbem_e_provider_not_registered"></span>**\_provedor WBEM \_ E \_ não \_ registrado**</span><span class="sxs-lookup"><span data-stu-id="41d1d-529"><span id="WBEM_E_PROVIDER_NOT_REGISTERED"></span><span id="wbem_e_provider_not_registered"></span>**WBEM\_E\_PROVIDER\_NOT\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-530">2147750021 (0x80041085)</span><span class="sxs-lookup"><span data-stu-id="41d1d-530">2147750021 (0x80041085)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-531">O provedor não foi registrado.</span><span class="sxs-lookup"><span data-stu-id="41d1d-531">Provider was not registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-532"><span id="WBEM_E_FATAL_TRANSPORT_ERROR"></span><span id="wbem_e_fatal_transport_error"></span>**\_erro de \_ \_ transporte fatal \_ de WBEM E**</span><span class="sxs-lookup"><span data-stu-id="41d1d-532"><span id="WBEM_E_FATAL_TRANSPORT_ERROR"></span><span id="wbem_e_fatal_transport_error"></span>**WBEM\_E\_FATAL\_TRANSPORT\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-533">2147750022 (0x80041086)</span><span class="sxs-lookup"><span data-stu-id="41d1d-533">2147750022 (0x80041086)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-534">Ocorreu um erro de transporte fatal.</span><span class="sxs-lookup"><span data-stu-id="41d1d-534">A fatal transport error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-535"><span id="WBEM_E_ENCRYPTED_CONNECTION_REQUIRED"></span><span id="wbem_e_encrypted_connection_required"></span>**conexão de WBEM \_ E \_ criptografada \_ \_ necessária**</span><span class="sxs-lookup"><span data-stu-id="41d1d-535"><span id="WBEM_E_ENCRYPTED_CONNECTION_REQUIRED"></span><span id="wbem_e_encrypted_connection_required"></span>**WBEM\_E\_ENCRYPTED\_CONNECTION\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-536">2147750023 (0x80041087)</span><span class="sxs-lookup"><span data-stu-id="41d1d-536">2147750023 (0x80041087)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-537">O usuário tentou definir um nome de computador ou domínio sem uma conexão criptografada.</span><span class="sxs-lookup"><span data-stu-id="41d1d-537">User attempted to set a computer name or domain without an encrypted connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-538"><span id="WBEM_E_PROVIDER_TIMED_OUT"></span><span id="wbem_e_provider_timed_out"></span>**o \_ provedor WBEM E \_ \_ atingiu o tempo \_ limite**</span><span class="sxs-lookup"><span data-stu-id="41d1d-538"><span id="WBEM_E_PROVIDER_TIMED_OUT"></span><span id="wbem_e_provider_timed_out"></span>**WBEM\_E\_PROVIDER\_TIMED\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-539">2147750024 (0x80041088)</span><span class="sxs-lookup"><span data-stu-id="41d1d-539">2147750024 (0x80041088)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-540">Um provedor não pôde relatar resultados dentro do tempo limite especificado.</span><span class="sxs-lookup"><span data-stu-id="41d1d-540">A provider failed to report results within the specified timeout.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-541"><span id="WBEM_E_NO_KEY"></span><span id="wbem_e_no_key"></span>**\_ \_ nenhuma \_ chave do WBEM E**</span><span class="sxs-lookup"><span data-stu-id="41d1d-541"><span id="WBEM_E_NO_KEY"></span><span id="wbem_e_no_key"></span>**WBEM\_E\_NO\_KEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-542">2147750025 (0x80041089)</span><span class="sxs-lookup"><span data-stu-id="41d1d-542">2147750025 (0x80041089)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-543">O usuário tentou colocar uma instância sem chave definida.</span><span class="sxs-lookup"><span data-stu-id="41d1d-543">User attempted to put an instance with no defined key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-544"><span id="WBEM_E_PROVIDER_DISABLED"></span><span id="wbem_e_provider_disabled"></span>**\_provedor WBEM \_ E \_ desabilitado**</span><span class="sxs-lookup"><span data-stu-id="41d1d-544"><span id="WBEM_E_PROVIDER_DISABLED"></span><span id="wbem_e_provider_disabled"></span>**WBEM\_E\_PROVIDER\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-545">2147750026 (0x8004108A)</span><span class="sxs-lookup"><span data-stu-id="41d1d-545">2147750026 (0x8004108A)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-546">O usuário tentou registrar uma instância do provedor, mas o servidor COM da instância do provedor foi descarregado.</span><span class="sxs-lookup"><span data-stu-id="41d1d-546">User attempted to register a provider instance but the COM server for the provider instance was unloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-547"><span id="WBEMESS_E_REGISTRATION_TOO_BROAD"></span><span id="wbemess_e_registration_too_broad"></span>**WBEMESS \_ E \_ registro \_ muito \_ amplo**</span><span class="sxs-lookup"><span data-stu-id="41d1d-547"><span id="WBEMESS_E_REGISTRATION_TOO_BROAD"></span><span id="wbemess_e_registration_too_broad"></span>**WBEMESS\_E\_REGISTRATION\_TOO\_BROAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-548">2147753985 (0x80042001)</span><span class="sxs-lookup"><span data-stu-id="41d1d-548">2147753985 (0x80042001)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-549">O registro do provedor se sobrepõe ao domínio de evento do sistema.</span><span class="sxs-lookup"><span data-stu-id="41d1d-549">Provider registration overlaps with the system event domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-550"><span id="WBEMESS_E_REGISTRATION_TOO_PRECISE"></span><span id="wbemess_e_registration_too_precise"></span>**WBEMESS \_ E \_ registro \_ muito \_ preciso**</span><span class="sxs-lookup"><span data-stu-id="41d1d-550"><span id="WBEMESS_E_REGISTRATION_TOO_PRECISE"></span><span id="wbemess_e_registration_too_precise"></span>**WBEMESS\_E\_REGISTRATION\_TOO\_PRECISE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-551">2147753986 (0x80042002)</span><span class="sxs-lookup"><span data-stu-id="41d1d-551">2147753986 (0x80042002)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-552">Uma cláusula WITHIN não foi usada nesta consulta.</span><span class="sxs-lookup"><span data-stu-id="41d1d-552">A WITHIN clause was not used in this query.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-553"><span id="WBEMESS_E_AUTHZ_NOT_PRIVILEGED"></span><span id="wbemess_e_authz_not_privileged"></span>**WBEMESS \_ E \_ AUTHZ \_ não \_ privilegiado**</span><span class="sxs-lookup"><span data-stu-id="41d1d-553"><span id="WBEMESS_E_AUTHZ_NOT_PRIVILEGED"></span><span id="wbemess_e_authz_not_privileged"></span>**WBEMESS\_E\_AUTHZ\_NOT\_PRIVILEGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-554">2147753987 (0x80042003)</span><span class="sxs-lookup"><span data-stu-id="41d1d-554">2147753987 (0x80042003)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-555">Este computador não tem as permissões de domínio necessárias para dar suporte às funções de segurança relacionadas à instância de assinatura criada.</span><span class="sxs-lookup"><span data-stu-id="41d1d-555">This computer does not have the necessary domain permissions to support the security functions that relate to the created subscription instance.</span></span> <span data-ttu-id="41d1d-556">Contate o administrador de domínio para que este computador seja adicionado ao grupo de acesso de autorização do Windows.</span><span class="sxs-lookup"><span data-stu-id="41d1d-556">Contact the Domain Administrator to get this computer added to the Windows Authorization Access Group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-557"><span id="WBEM_E_RETRY_LATER"></span><span id="wbem_e_retry_later"></span>**WBEM \_ E \_ tentar novamente \_ mais tarde**</span><span class="sxs-lookup"><span data-stu-id="41d1d-557"><span id="WBEM_E_RETRY_LATER"></span><span id="wbem_e_retry_later"></span>**WBEM\_E\_RETRY\_LATER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-558">2147758081 (0x80043001)</span><span class="sxs-lookup"><span data-stu-id="41d1d-558">2147758081 (0x80043001)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-559">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="41d1d-559">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-560"><span id="WBEM_E_RESOURCE_CONTENTION"></span><span id="wbem_e_resource_contention"></span>**contenção de \_ recurso WBEM E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-560"><span id="WBEM_E_RESOURCE_CONTENTION"></span><span id="wbem_e_resource_contention"></span>**WBEM\_E\_RESOURCE\_CONTENTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-561">2147758082 (0x80043002)</span><span class="sxs-lookup"><span data-stu-id="41d1d-561">2147758082 (0x80043002)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-562">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="41d1d-562">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-563"><span id="WBEMMOF_E_EXPECTED_QUALIFIER_NAME"></span><span id="wbemmof_e_expected_qualifier_name"></span>**WBEMMOF \_ E \_ \_ nome do qualificador esperado \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-563"><span id="WBEMMOF_E_EXPECTED_QUALIFIER_NAME"></span><span id="wbemmof_e_expected_qualifier_name"></span>**WBEMMOF\_E\_EXPECTED\_QUALIFIER\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-564">2147762177 (0x80044001)</span><span class="sxs-lookup"><span data-stu-id="41d1d-564">2147762177 (0x80044001)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-565">Esperado um nome de qualificador.</span><span class="sxs-lookup"><span data-stu-id="41d1d-565">Expected a qualifier name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-566"><span id="WBEMMOF_E_EXPECTED_SEMI"></span><span id="wbemmof_e_expected_semi"></span>**WBEMMOF \_ E \_ \_ semi esperado**</span><span class="sxs-lookup"><span data-stu-id="41d1d-566"><span id="WBEMMOF_E_EXPECTED_SEMI"></span><span id="wbemmof_e_expected_semi"></span>**WBEMMOF\_E\_EXPECTED\_SEMI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-567">2147762178 (0x80044002)</span><span class="sxs-lookup"><span data-stu-id="41d1d-567">2147762178 (0x80044002)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-568">Ponto-e-vírgula esperado ou ' = '.</span><span class="sxs-lookup"><span data-stu-id="41d1d-568">Expected semicolon or '='.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-569"><span id="WBEMMOF_E_EXPECTED_OPEN_BRACE"></span><span id="wbemmof_e_expected_open_brace"></span>**WBEMMOF \_ E \_ \_ chave de abertura esperada \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-569"><span id="WBEMMOF_E_EXPECTED_OPEN_BRACE"></span><span id="wbemmof_e_expected_open_brace"></span>**WBEMMOF\_E\_EXPECTED\_OPEN\_BRACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-570">2147762179 (0x80044003)</span><span class="sxs-lookup"><span data-stu-id="41d1d-570">2147762179 (0x80044003)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-571">Chave de abertura esperada.</span><span class="sxs-lookup"><span data-stu-id="41d1d-571">Expected an opening brace.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-572"><span id="WBEMMOF_E_EXPECTED_CLOSE_BRACE"></span><span id="wbemmof_e_expected_close_brace"></span>**WBEMMOF \_ E \_ \_ chave de fechamento esperada \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-572"><span id="WBEMMOF_E_EXPECTED_CLOSE_BRACE"></span><span id="wbemmof_e_expected_close_brace"></span>**WBEMMOF\_E\_EXPECTED\_CLOSE\_BRACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-573">2147762180 (0x80044004)</span><span class="sxs-lookup"><span data-stu-id="41d1d-573">2147762180 (0x80044004)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-574">Chave de fechamento ausente ou elemento de matriz inválido.</span><span class="sxs-lookup"><span data-stu-id="41d1d-574">Missing closing brace or an illegal array element.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-575"><span id="WBEMMOF_E_EXPECTED_CLOSE_BRACKET"></span><span id="wbemmof_e_expected_close_bracket"></span>**WBEMMOF \_ E \_ \_ colchete de fechamento esperado \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-575"><span id="WBEMMOF_E_EXPECTED_CLOSE_BRACKET"></span><span id="wbemmof_e_expected_close_bracket"></span>**WBEMMOF\_E\_EXPECTED\_CLOSE\_BRACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-576">2147762181 (0x80044005)</span><span class="sxs-lookup"><span data-stu-id="41d1d-576">2147762181 (0x80044005)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-577">Esperado um colchete de fechamento.</span><span class="sxs-lookup"><span data-stu-id="41d1d-577">Expected a closing bracket.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-578"><span id="WBEMMOF_E_EXPECTED_CLOSE_PAREN"></span><span id="wbemmof_e_expected_close_paren"></span>**WBEMMOF \_ E \_ \_ parêntese de fechamento esperado \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-578"><span id="WBEMMOF_E_EXPECTED_CLOSE_PAREN"></span><span id="wbemmof_e_expected_close_paren"></span>**WBEMMOF\_E\_EXPECTED\_CLOSE\_PAREN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-579">2147762182 (0x80044006)</span><span class="sxs-lookup"><span data-stu-id="41d1d-579">2147762182 (0x80044006)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-580">Parêntese de fechamento esperado.</span><span class="sxs-lookup"><span data-stu-id="41d1d-580">Expected closing parenthesis.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-581"><span id="WBEMMOF_E_ILLEGAL_CONSTANT_VALUE"></span><span id="wbemmof_e_illegal_constant_value"></span>**WBEMMOF \_ E \_ \_ valor constante \_ ilegal**</span><span class="sxs-lookup"><span data-stu-id="41d1d-581"><span id="WBEMMOF_E_ILLEGAL_CONSTANT_VALUE"></span><span id="wbemmof_e_illegal_constant_value"></span>**WBEMMOF\_E\_ILLEGAL\_CONSTANT\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-582">2147762183 (0x80044007)</span><span class="sxs-lookup"><span data-stu-id="41d1d-582">2147762183 (0x80044007)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-583">Valor numérico fora do intervalo ou cadeias de caracteres sem aspas.</span><span class="sxs-lookup"><span data-stu-id="41d1d-583">Numeric value out of range or strings without quotes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-584"><span id="WBEMMOF_E_EXPECTED_TYPE_IDENTIFIER"></span><span id="wbemmof_e_expected_type_identifier"></span>**WBEMMOF \_ E \_ \_ identificador de tipo esperado \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-584"><span id="WBEMMOF_E_EXPECTED_TYPE_IDENTIFIER"></span><span id="wbemmof_e_expected_type_identifier"></span>**WBEMMOF\_E\_EXPECTED\_TYPE\_IDENTIFIER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-585">2147762184 (0x80044008)</span><span class="sxs-lookup"><span data-stu-id="41d1d-585">2147762184 (0x80044008)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-586">Esperado um identificador de tipo.</span><span class="sxs-lookup"><span data-stu-id="41d1d-586">Expected a type identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-587"><span id="WBEMMOF_E_EXPECTED_OPEN_PAREN"></span><span id="wbemmof_e_expected_open_paren"></span>**WBEMMOF \_ E \_ esperado \_ abrir \_ parênteses**</span><span class="sxs-lookup"><span data-stu-id="41d1d-587"><span id="WBEMMOF_E_EXPECTED_OPEN_PAREN"></span><span id="wbemmof_e_expected_open_paren"></span>**WBEMMOF\_E\_EXPECTED\_OPEN\_PAREN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-588">2147762185 (0x80044009)</span><span class="sxs-lookup"><span data-stu-id="41d1d-588">2147762185 (0x80044009)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-589">Esperado um parêntese de abertura.</span><span class="sxs-lookup"><span data-stu-id="41d1d-589">Expected an open parenthesis.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-590"><span id="WBEMMOF_E_UNRECOGNIZED_TOKEN"></span><span id="wbemmof_e_unrecognized_token"></span>**\_token WBEMMOF E \_ não reconhecido \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-590"><span id="WBEMMOF_E_UNRECOGNIZED_TOKEN"></span><span id="wbemmof_e_unrecognized_token"></span>**WBEMMOF\_E\_UNRECOGNIZED\_TOKEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-591">2147762186 (0x8004400A)</span><span class="sxs-lookup"><span data-stu-id="41d1d-591">2147762186 (0x8004400A)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-592">Token inesperado no arquivo.</span><span class="sxs-lookup"><span data-stu-id="41d1d-592">Unexpected token in the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-593"><span id="WBEMMOF_E_UNRECOGNIZED_TYPE"></span><span id="wbemmof_e_unrecognized_type"></span>**WBEMMOF \_ E \_ tipo não reconhecido \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-593"><span id="WBEMMOF_E_UNRECOGNIZED_TYPE"></span><span id="wbemmof_e_unrecognized_type"></span>**WBEMMOF\_E\_UNRECOGNIZED\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-594">2147762187 (0x8004400B)</span><span class="sxs-lookup"><span data-stu-id="41d1d-594">2147762187 (0x8004400B)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-595">Identificador de tipo não reconhecido ou sem suporte.</span><span class="sxs-lookup"><span data-stu-id="41d1d-595">Unrecognized or unsupported type identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-596"><span id="WBEMMOF_E_EXPECTED_PROPERTY_NAME"></span><span id="wbemmof_e_expected_property_name"></span>**WBEMMOF \_ E \_ \_ nome da propriedade esperado \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-596"><span id="WBEMMOF_E_EXPECTED_PROPERTY_NAME"></span><span id="wbemmof_e_expected_property_name"></span>**WBEMMOF\_E\_EXPECTED\_PROPERTY\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-597">2147762187 (0x8004400B)</span><span class="sxs-lookup"><span data-stu-id="41d1d-597">2147762187 (0x8004400B)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-598">Propriedade ou nome de método esperado.</span><span class="sxs-lookup"><span data-stu-id="41d1d-598">Expected property or method name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-599"><span id="WBEMMOF_E_TYPEDEF_NOT_SUPPORTED"></span><span id="wbemmof_e_typedef_not_supported"></span>**\_ \_ \_ não \_ há suporte para WBEMMOF E TYPEDEF**</span><span class="sxs-lookup"><span data-stu-id="41d1d-599"><span id="WBEMMOF_E_TYPEDEF_NOT_SUPPORTED"></span><span id="wbemmof_e_typedef_not_supported"></span>**WBEMMOF\_E\_TYPEDEF\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-600">2147762189 (0x8004400D)</span><span class="sxs-lookup"><span data-stu-id="41d1d-600">2147762189 (0x8004400D)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-601">Não há suporte para TYPEDEFs e tipos enumerados.</span><span class="sxs-lookup"><span data-stu-id="41d1d-601">Typedefs and enumerated types are not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-602"><span id="WBEMMOF_E_UNEXPECTED_ALIAS"></span><span id="wbemmof_e_unexpected_alias"></span>**WBEMMOF \_ E \_ alias inesperado \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-602"><span id="WBEMMOF_E_UNEXPECTED_ALIAS"></span><span id="wbemmof_e_unexpected_alias"></span>**WBEMMOF\_E\_UNEXPECTED\_ALIAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-603">2147762190 (0x8004400E)</span><span class="sxs-lookup"><span data-stu-id="41d1d-603">2147762190 (0x8004400E)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-604">Somente uma referência a um objeto de classe pode ter um valor de alias.</span><span class="sxs-lookup"><span data-stu-id="41d1d-604">Only a reference to a class object can have an alias value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-605"><span id="WBEMMOF_E_UNEXPECTED_ARRAY_INIT"></span><span id="wbemmof_e_unexpected_array_init"></span>**WBEMMOF \_ E \_ \_ inicialização de matriz inesperada \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-605"><span id="WBEMMOF_E_UNEXPECTED_ARRAY_INIT"></span><span id="wbemmof_e_unexpected_array_init"></span>**WBEMMOF\_E\_UNEXPECTED\_ARRAY\_INIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-606">2147762191 (0x8004400F)</span><span class="sxs-lookup"><span data-stu-id="41d1d-606">2147762191 (0x8004400F)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-607">Inicialização de matriz inesperada.</span><span class="sxs-lookup"><span data-stu-id="41d1d-607">Unexpected array initialization.</span></span> <span data-ttu-id="41d1d-608">As matrizes devem ser declaradas com \[ \] .</span><span class="sxs-lookup"><span data-stu-id="41d1d-608">Arrays must be declared with \[\].</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-609"><span id="WBEMMOF_E_INVALID_AMENDMENT_SYNTAX"></span><span id="wbemmof_e_invalid_amendment_syntax"></span>**WBEMMOF \_ E \_ \_ sintaxe de emenda inválida \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-609"><span id="WBEMMOF_E_INVALID_AMENDMENT_SYNTAX"></span><span id="wbemmof_e_invalid_amendment_syntax"></span>**WBEMMOF\_E\_INVALID\_AMENDMENT\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-610">2147762192 (0x80044010)</span><span class="sxs-lookup"><span data-stu-id="41d1d-610">2147762192 (0x80044010)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-611">A sintaxe do caminho do namespace não é válida.</span><span class="sxs-lookup"><span data-stu-id="41d1d-611">Namespace path syntax is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-612"><span id="WBEMMOF_E_INVALID_DUPLICATE_AMENDMENT"></span><span id="wbemmof_e_invalid_duplicate_amendment"></span>**WBEMMOF \_ E \_ \_ alteração de duplicação inválida \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-612"><span id="WBEMMOF_E_INVALID_DUPLICATE_AMENDMENT"></span><span id="wbemmof_e_invalid_duplicate_amendment"></span>**WBEMMOF\_E\_INVALID\_DUPLICATE\_AMENDMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-613">2147762193 (0x80044011)</span><span class="sxs-lookup"><span data-stu-id="41d1d-613">2147762193 (0x80044011)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-614">Duplicar especificadores de emenda.</span><span class="sxs-lookup"><span data-stu-id="41d1d-614">Duplicate amendment specifiers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-615"><span id="WBEMMOF_E_INVALID_PRAGMA"></span><span id="wbemmof_e_invalid_pragma"></span>**WBEMMOF \_ E \_ \_ pragma inválido**</span><span class="sxs-lookup"><span data-stu-id="41d1d-615"><span id="WBEMMOF_E_INVALID_PRAGMA"></span><span id="wbemmof_e_invalid_pragma"></span>**WBEMMOF\_E\_INVALID\_PRAGMA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-616">2147762194 (0x80044012)</span><span class="sxs-lookup"><span data-stu-id="41d1d-616">2147762194 (0x80044012)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-617">[ \# pragma](pragma-namespace.md) deve ser seguido por uma palavra-chave válida.</span><span class="sxs-lookup"><span data-stu-id="41d1d-617">[\#pragma](pragma-namespace.md) must be followed by a valid keyword.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-618"><span id="WBEMMOF_E_INVALID_NAMESPACE_SYNTAX"></span><span id="wbemmof_e_invalid_namespace_syntax"></span>**WBEMMOF \_ E \_ \_ sintaxe de namespace inválida \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-618"><span id="WBEMMOF_E_INVALID_NAMESPACE_SYNTAX"></span><span id="wbemmof_e_invalid_namespace_syntax"></span>**WBEMMOF\_E\_INVALID\_NAMESPACE\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-619">2147762195 (0x80044013)</span><span class="sxs-lookup"><span data-stu-id="41d1d-619">2147762195 (0x80044013)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-620">A sintaxe do caminho do namespace não é válida.</span><span class="sxs-lookup"><span data-stu-id="41d1d-620">Namespace path syntax is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-621"><span id="WBEMMOF_E_EXPECTED_CLASS_NAME"></span><span id="wbemmof_e_expected_class_name"></span>**WBEMMOF \_ E \_ \_ nome de classe esperado \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-621"><span id="WBEMMOF_E_EXPECTED_CLASS_NAME"></span><span id="wbemmof_e_expected_class_name"></span>**WBEMMOF\_E\_EXPECTED\_CLASS\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-622">2147762196 (0x80044014)</span><span class="sxs-lookup"><span data-stu-id="41d1d-622">2147762196 (0x80044014)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-623">O caractere inesperado no nome da classe deve ser um identificador.</span><span class="sxs-lookup"><span data-stu-id="41d1d-623">Unexpected character in class name must be an identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-624"><span id="WBEMMOF_E_TYPE_MISMATCH"></span><span id="wbemmof_e_type_mismatch"></span>**incompatibilidade de \_ tipo E WBEMMOF \_ \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-624"><span id="WBEMMOF_E_TYPE_MISMATCH"></span><span id="wbemmof_e_type_mismatch"></span>**WBEMMOF\_E\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-625">2147762197 (0x80044015)</span><span class="sxs-lookup"><span data-stu-id="41d1d-625">2147762197 (0x80044015)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-626">O valor especificado não pode ser feito no tipo apropriado.</span><span class="sxs-lookup"><span data-stu-id="41d1d-626">The value specified cannot be made into the appropriate type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-627"><span id="WBEMMOF_E_EXPECTED_ALIAS_NAME"></span><span id="wbemmof_e_expected_alias_name"></span>**WBEMMOF \_ E \_ \_ nome de alias esperado \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-627"><span id="WBEMMOF_E_EXPECTED_ALIAS_NAME"></span><span id="wbemmof_e_expected_alias_name"></span>**WBEMMOF\_E\_EXPECTED\_ALIAS\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-628">2147762198 (0x80044016)</span><span class="sxs-lookup"><span data-stu-id="41d1d-628">2147762198 (0x80044016)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-629">Cifrão deve ser seguido por um nome de alias como um identificador.</span><span class="sxs-lookup"><span data-stu-id="41d1d-629">Dollar sign must be followed by an alias name as an identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-630"><span id="WBEMMOF_E_INVALID_CLASS_DECLARATION"></span><span id="wbemmof_e_invalid_class_declaration"></span>**WBEMMOF \_ E \_ \_ declaração de classe inválida \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-630"><span id="WBEMMOF_E_INVALID_CLASS_DECLARATION"></span><span id="wbemmof_e_invalid_class_declaration"></span>**WBEMMOF\_E\_INVALID\_CLASS\_DECLARATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-631">2147762199 (0x80044017)</span><span class="sxs-lookup"><span data-stu-id="41d1d-631">2147762199 (0x80044017)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-632">Declaração de classe inválida.</span><span class="sxs-lookup"><span data-stu-id="41d1d-632">Class declaration is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-633"><span id="WBEMMOF_E_INVALID_INSTANCE_DECLARATION"></span><span id="wbemmof_e_invalid_instance_declaration"></span>**WBEMMOF \_ E \_ \_ declaração de instância inválida \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-633"><span id="WBEMMOF_E_INVALID_INSTANCE_DECLARATION"></span><span id="wbemmof_e_invalid_instance_declaration"></span>**WBEMMOF\_E\_INVALID\_INSTANCE\_DECLARATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-634">2147762200 (0x80044018)</span><span class="sxs-lookup"><span data-stu-id="41d1d-634">2147762200 (0x80044018)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-635">A declaração de instância não é válida.</span><span class="sxs-lookup"><span data-stu-id="41d1d-635">The instance declaration is not valid.</span></span> <span data-ttu-id="41d1d-636">Ele deve começar com "instance of"</span><span class="sxs-lookup"><span data-stu-id="41d1d-636">It must start with "instance of"</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-637"><span id="WBEMMOF_E_EXPECTED_DOLLAR"></span><span id="wbemmof_e_expected_dollar"></span>**WBEMMOF \_ E \_ \_ dólar esperado**</span><span class="sxs-lookup"><span data-stu-id="41d1d-637"><span id="WBEMMOF_E_EXPECTED_DOLLAR"></span><span id="wbemmof_e_expected_dollar"></span>**WBEMMOF\_E\_EXPECTED\_DOLLAR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-638">2147762201 (0x80044019)</span><span class="sxs-lookup"><span data-stu-id="41d1d-638">2147762201 (0x80044019)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-639">Sinal de dólar esperado.</span><span class="sxs-lookup"><span data-stu-id="41d1d-639">Expected dollar sign.</span></span> <span data-ttu-id="41d1d-640">Um alias no formato "$name" deve seguir a palavra-chave "as".</span><span class="sxs-lookup"><span data-stu-id="41d1d-640">An alias in the form "$name" must follow the "as" keyword.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-641"><span id="WBEMMOF_E_CIMTYPE_QUALIFIER"></span><span id="wbemmof_e_cimtype_qualifier"></span>**\_ \_ qualificador WBEMMOF E CimType \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-641"><span id="WBEMMOF_E_CIMTYPE_QUALIFIER"></span><span id="wbemmof_e_cimtype_qualifier"></span>**WBEMMOF\_E\_CIMTYPE\_QUALIFIER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-642">2147762202 (0x8004401A)</span><span class="sxs-lookup"><span data-stu-id="41d1d-642">2147762202 (0x8004401A)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-643">O qualificador "CIMTYPE" não pode ser especificado diretamente em um arquivo MOF.</span><span class="sxs-lookup"><span data-stu-id="41d1d-643">"CIMTYPE" qualifier cannot be specified directly in a MOF file.</span></span> <span data-ttu-id="41d1d-644">Use a notação de tipo padrão.</span><span class="sxs-lookup"><span data-stu-id="41d1d-644">Use standard type notation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-645"><span id="WBEMMOF_E_DUPLICATE_PROPERTY"></span><span id="wbemmof_e_duplicate_property"></span>**WBEMMOF \_ E \_ duplicar \_ Propriedade**</span><span class="sxs-lookup"><span data-stu-id="41d1d-645"><span id="WBEMMOF_E_DUPLICATE_PROPERTY"></span><span id="wbemmof_e_duplicate_property"></span>**WBEMMOF\_E\_DUPLICATE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-646">2147762203 (0x8004401B)</span><span class="sxs-lookup"><span data-stu-id="41d1d-646">2147762203 (0x8004401B)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-647">Nome de propriedade duplicado encontrado no MOF.</span><span class="sxs-lookup"><span data-stu-id="41d1d-647">Duplicate property name was found in the MOF.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-648"><span id="WBEMMOF_E_INVALID_NAMESPACE_SPECIFICATION"></span><span id="wbemmof_e_invalid_namespace_specification"></span>**WBEMMOF \_ E \_ \_ especificação de namespace inválido \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-648"><span id="WBEMMOF_E_INVALID_NAMESPACE_SPECIFICATION"></span><span id="wbemmof_e_invalid_namespace_specification"></span>**WBEMMOF\_E\_INVALID\_NAMESPACE\_SPECIFICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-649">2147762204 (0x8004401C)</span><span class="sxs-lookup"><span data-stu-id="41d1d-649">2147762204 (0x8004401C)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-650">A sintaxe do namespace não é válida.</span><span class="sxs-lookup"><span data-stu-id="41d1d-650">Namespace syntax is not valid.</span></span> <span data-ttu-id="41d1d-651">Referências a outros servidores não são permitidas.</span><span class="sxs-lookup"><span data-stu-id="41d1d-651">References to other servers are not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-652"><span id="WBEMMOF_E_OUT_OF_RANGE"></span><span id="wbemmof_e_out_of_range"></span>**WBEMMOF \_ E \_ fora \_ do \_ intervalo**</span><span class="sxs-lookup"><span data-stu-id="41d1d-652"><span id="WBEMMOF_E_OUT_OF_RANGE"></span><span id="wbemmof_e_out_of_range"></span>**WBEMMOF\_E\_OUT\_OF\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-653">2147762205 (0x8004401D)</span><span class="sxs-lookup"><span data-stu-id="41d1d-653">2147762205 (0x8004401D)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-654">Valor fora do intervalo.</span><span class="sxs-lookup"><span data-stu-id="41d1d-654">Value out of range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-655"><span id="WBEMMOF_E_INVALID_FILE"></span><span id="wbemmof_e_invalid_file"></span>**WBEMMOF \_ E \_ \_ arquivo inválido**</span><span class="sxs-lookup"><span data-stu-id="41d1d-655"><span id="WBEMMOF_E_INVALID_FILE"></span><span id="wbemmof_e_invalid_file"></span>**WBEMMOF\_E\_INVALID\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-656">2147762206 (0x8004401E)</span><span class="sxs-lookup"><span data-stu-id="41d1d-656">2147762206 (0x8004401E)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-657">O arquivo não é um arquivo MOF de texto válido ou arquivo MOF binário.</span><span class="sxs-lookup"><span data-stu-id="41d1d-657">The file is not a valid text MOF file or binary MOF file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-658"><span id="WBEMMOF_E_ALIASES_IN_EMBEDDED"></span><span id="wbemmof_e_aliases_in_embedded"></span>**WBEMMOF \_ E \_ aliases \_ no \_ Embedded**</span><span class="sxs-lookup"><span data-stu-id="41d1d-658"><span id="WBEMMOF_E_ALIASES_IN_EMBEDDED"></span><span id="wbemmof_e_aliases_in_embedded"></span>**WBEMMOF\_E\_ALIASES\_IN\_EMBEDDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-659">2147762207 (0x8004401F)</span><span class="sxs-lookup"><span data-stu-id="41d1d-659">2147762207 (0x8004401F)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-660">Objetos inseridos não podem ser aliases.</span><span class="sxs-lookup"><span data-stu-id="41d1d-660">Embedded objects cannot be aliases.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-661"><span id="WBEMMOF_E_NULL_ARRAY_ELEM"></span><span id="wbemmof_e_null_array_elem"></span>**\_matriz WBEMMOF \_ E \_ \_ elem nula**</span><span class="sxs-lookup"><span data-stu-id="41d1d-661"><span id="WBEMMOF_E_NULL_ARRAY_ELEM"></span><span id="wbemmof_e_null_array_elem"></span>**WBEMMOF\_E\_NULL\_ARRAY\_ELEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-662">2147762208 (0x80044020)</span><span class="sxs-lookup"><span data-stu-id="41d1d-662">2147762208 (0x80044020)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-663">Não há suporte para elementos nulos em uma matriz.</span><span class="sxs-lookup"><span data-stu-id="41d1d-663">NULL elements in an array are not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-664"><span id="WBEMMOF_E_DUPLICATE_QUALIFIER"></span><span id="wbemmof_e_duplicate_qualifier"></span>**\_ \_ qualificador WBEMMOF E duplicado \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-664"><span id="WBEMMOF_E_DUPLICATE_QUALIFIER"></span><span id="wbemmof_e_duplicate_qualifier"></span>**WBEMMOF\_E\_DUPLICATE\_QUALIFIER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-665">2147762209 (0x80044021)</span><span class="sxs-lookup"><span data-stu-id="41d1d-665">2147762209 (0x80044021)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-666">O qualificador foi usado mais de uma vez no objeto.</span><span class="sxs-lookup"><span data-stu-id="41d1d-666">Qualifier was used more than once on the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-667"><span id="WBEMMOF_E_EXPECTED_FLAVOR_TYPE"></span><span id="wbemmof_e_expected_flavor_type"></span>**WBEMMOF \_ E \_ \_ tipo de flavor esperado \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-667"><span id="WBEMMOF_E_EXPECTED_FLAVOR_TYPE"></span><span id="wbemmof_e_expected_flavor_type"></span>**WBEMMOF\_E\_EXPECTED\_FLAVOR\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-668">2147762210 (0x80044022)</span><span class="sxs-lookup"><span data-stu-id="41d1d-668">2147762210 (0x80044022)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-669">Era esperado um tipo de flavor como **ToInstance**, **ToSubClass**, **EnableOverride** ou **DisableOverride**.</span><span class="sxs-lookup"><span data-stu-id="41d1d-669">Expected a flavor type such as **ToInstance**, **ToSubClass**, **EnableOverride**, or **DisableOverride**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-670"><span id="WBEMMOF_E_INCOMPATIBLE_FLAVOR_TYPES"></span><span id="wbemmof_e_incompatible_flavor_types"></span>**\_tipos de \_ tipo incompatíveis E \_ WBEMMOF \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-670"><span id="WBEMMOF_E_INCOMPATIBLE_FLAVOR_TYPES"></span><span id="wbemmof_e_incompatible_flavor_types"></span>**WBEMMOF\_E\_INCOMPATIBLE\_FLAVOR\_TYPES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-671">2147762211 (0x80044023)</span><span class="sxs-lookup"><span data-stu-id="41d1d-671">2147762211 (0x80044023)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-672">A combinação de **EnableOverride** e **DisableOverride** no mesmo qualificador não é válida.</span><span class="sxs-lookup"><span data-stu-id="41d1d-672">Combining **EnableOverride** and **DisableOverride** on same qualifier is not legal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-673"><span id="WBEMMOF_E_MULTIPLE_ALIASES"></span><span id="wbemmof_e_multiple_aliases"></span>**WBEMMOF \_ E \_ vários \_ aliases**</span><span class="sxs-lookup"><span data-stu-id="41d1d-673"><span id="WBEMMOF_E_MULTIPLE_ALIASES"></span><span id="wbemmof_e_multiple_aliases"></span>**WBEMMOF\_E\_MULTIPLE\_ALIASES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-674">2147762212 (0x80044024)</span><span class="sxs-lookup"><span data-stu-id="41d1d-674">2147762212 (0x80044024)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-675">Um alias não pode ser usado duas vezes.</span><span class="sxs-lookup"><span data-stu-id="41d1d-675">An alias cannot be used twice.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-676"><span id="WBEMMOF_E_INCOMPATIBLE_FLAVOR_TYPES2"></span><span id="wbemmof_e_incompatible_flavor_types2"></span>**\_ \_ \_ Tipo TYPES2 WBEMMOF E incompatível \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-676"><span id="WBEMMOF_E_INCOMPATIBLE_FLAVOR_TYPES2"></span><span id="wbemmof_e_incompatible_flavor_types2"></span>**WBEMMOF\_E\_INCOMPATIBLE\_FLAVOR\_TYPES2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-677">2147762213 (0x80044025)</span><span class="sxs-lookup"><span data-stu-id="41d1d-677">2147762213 (0x80044025)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-678">A combinação de **Restricted** e **ToInstance** ou **ToSubClass** não é válida.</span><span class="sxs-lookup"><span data-stu-id="41d1d-678">Combining **Restricted**, and **ToInstance** or **ToSubClass** is not legal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-679"><span id="WBEMMOF_E_NO_ARRAYS_RETURNED"></span><span id="wbemmof_e_no_arrays_returned"></span>**WBEMMOF \_ E \_ nenhuma \_ matriz \_ retornada**</span><span class="sxs-lookup"><span data-stu-id="41d1d-679"><span id="WBEMMOF_E_NO_ARRAYS_RETURNED"></span><span id="wbemmof_e_no_arrays_returned"></span>**WBEMMOF\_E\_NO\_ARRAYS\_RETURNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-680">2147762214 (0x80044026)</span><span class="sxs-lookup"><span data-stu-id="41d1d-680">2147762214 (0x80044026)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-681">Os métodos não podem retornar valores de matriz.</span><span class="sxs-lookup"><span data-stu-id="41d1d-681">Methods cannot return array values.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-682"><span id="WBEMMOF_E_MUST_BE_IN_OR_OUT"></span><span id="wbemmof_e_must_be_in_or_out"></span>**WBEMMOF \_ E \_ deve \_ estar \_ dentro \_ ou \_ fora**</span><span class="sxs-lookup"><span data-stu-id="41d1d-682"><span id="WBEMMOF_E_MUST_BE_IN_OR_OUT"></span><span id="wbemmof_e_must_be_in_or_out"></span>**WBEMMOF\_E\_MUST\_BE\_IN\_OR\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-683">2147762215 (0x80044027)</span><span class="sxs-lookup"><span data-stu-id="41d1d-683">2147762215 (0x80044027)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-684">Os argumentos devem ter um qualificador **de entrada** ou **saída** .</span><span class="sxs-lookup"><span data-stu-id="41d1d-684">Arguments must have an **In** or **Out** qualifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-685"><span id="WBEMMOF_E_INVALID_FLAGS_SYNTAX"></span><span id="wbemmof_e_invalid_flags_syntax"></span>**WBEMMOF \_ E \_ \_ sintaxe de sinalizadores inválidos \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-685"><span id="WBEMMOF_E_INVALID_FLAGS_SYNTAX"></span><span id="wbemmof_e_invalid_flags_syntax"></span>**WBEMMOF\_E\_INVALID\_FLAGS\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-686">2147762216 (0x80044028)</span><span class="sxs-lookup"><span data-stu-id="41d1d-686">2147762216 (0x80044028)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-687">A sintaxe de sinalizadores não é válida.</span><span class="sxs-lookup"><span data-stu-id="41d1d-687">Flags syntax is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-688"><span id="WBEMMOF_E_EXPECTED_BRACE_OR_BAD_TYPE"></span><span id="wbemmof_e_expected_brace_or_bad_type"></span>**WBEMMOF \_ E \_ chave esperada \_ \_ ou \_ tipo inadequado \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-688"><span id="WBEMMOF_E_EXPECTED_BRACE_OR_BAD_TYPE"></span><span id="wbemmof_e_expected_brace_or_bad_type"></span>**WBEMMOF\_E\_EXPECTED\_BRACE\_OR\_BAD\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-689">2147762217 (0x80044029)</span><span class="sxs-lookup"><span data-stu-id="41d1d-689">2147762217 (0x80044029)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-690">A chave final e o ponto-e-vírgula para uma classe estão ausentes.</span><span class="sxs-lookup"><span data-stu-id="41d1d-690">The final brace and semi-colon for a class are missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-691"><span id="WBEMMOF_E_UNSUPPORTED_CIMV22_QUAL_VALUE"></span><span id="wbemmof_e_unsupported_cimv22_qual_value"></span>**WBEMMOF \_ E \_ \_ \_ valor CIMV22 igual sem suporte \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-691"><span id="WBEMMOF_E_UNSUPPORTED_CIMV22_QUAL_VALUE"></span><span id="wbemmof_e_unsupported_cimv22_qual_value"></span>**WBEMMOF\_E\_UNSUPPORTED\_CIMV22\_QUAL\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-692">2147762218 (0x8004402A)</span><span class="sxs-lookup"><span data-stu-id="41d1d-692">2147762218 (0x8004402A)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-693">Não há suporte para um recurso de CIM versão 2,2 para um valor de qualificador.</span><span class="sxs-lookup"><span data-stu-id="41d1d-693">A CIM version 2.2 feature is not supported for a qualifier value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-694"><span id="WBEMMOF_E_UNSUPPORTED_CIMV22_DATA_TYPE"></span><span id="wbemmof_e_unsupported_cimv22_data_type"></span>**\_Tipo de \_ \_ dados CIMV22 WBEMMOF E sem suporte \_ \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-694"><span id="WBEMMOF_E_UNSUPPORTED_CIMV22_DATA_TYPE"></span><span id="wbemmof_e_unsupported_cimv22_data_type"></span>**WBEMMOF\_E\_UNSUPPORTED\_CIMV22\_DATA\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-695">2147762219 (0x8004402B)</span><span class="sxs-lookup"><span data-stu-id="41d1d-695">2147762219 (0x8004402B)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-696">Não há suporte para o tipo de dados CIM versão 2,2.</span><span class="sxs-lookup"><span data-stu-id="41d1d-696">The CIM version 2.2 data type is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-697"><span id="WBEMMOF_E_INVALID_DELETEINSTANCE_SYNTAX"></span><span id="wbemmof_e_invalid_deleteinstance_syntax"></span>**\_sintaxe de DELETEINSTANCE WBEMMOF E \_ inválida \_ \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-697"><span id="WBEMMOF_E_INVALID_DELETEINSTANCE_SYNTAX"></span><span id="wbemmof_e_invalid_deleteinstance_syntax"></span>**WBEMMOF\_E\_INVALID\_DELETEINSTANCE\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-698">2147762220 (0x8004402C)</span><span class="sxs-lookup"><span data-stu-id="41d1d-698">2147762220 (0x8004402C)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-699">A sintaxe da instância de exclusão não é válida.</span><span class="sxs-lookup"><span data-stu-id="41d1d-699">The delete instance syntax is not valid.</span></span> <span data-ttu-id="41d1d-700">Deve ser `#pragma DeleteInstance("instancepath", FAIL|NOFAIL)`</span><span class="sxs-lookup"><span data-stu-id="41d1d-700">It should be `#pragma DeleteInstance("instancepath", FAIL|NOFAIL)`</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-701"><span id="WBEMMOF_E_INVALID_QUALIFIER_SYNTAX"></span><span id="wbemmof_e_invalid_qualifier_syntax"></span>**WBEMMOF \_ E \_ \_ sintaxe de qualificador inválida \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-701"><span id="WBEMMOF_E_INVALID_QUALIFIER_SYNTAX"></span><span id="wbemmof_e_invalid_qualifier_syntax"></span>**WBEMMOF\_E\_INVALID\_QUALIFIER\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-702">2147762221 (0x8004402D)</span><span class="sxs-lookup"><span data-stu-id="41d1d-702">2147762221 (0x8004402D)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-703">A sintaxe do qualificador não é válida.</span><span class="sxs-lookup"><span data-stu-id="41d1d-703">The qualifier syntax is not valid.</span></span> <span data-ttu-id="41d1d-704">Ela deverá ser `qualifiername:type=value,scope(class|instance), flavorname`.</span><span class="sxs-lookup"><span data-stu-id="41d1d-704">It should be `qualifiername:type=value,scope(class|instance), flavorname`.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-705"><span id="WBEMMOF_E_QUALIFIER_USED_OUTSIDE_SCOPE"></span><span id="wbemmof_e_qualifier_used_outside_scope"></span>**\_ \_ qualificador WBEMMOF E \_ usado fora do \_ \_ escopo**</span><span class="sxs-lookup"><span data-stu-id="41d1d-705"><span id="WBEMMOF_E_QUALIFIER_USED_OUTSIDE_SCOPE"></span><span id="wbemmof_e_qualifier_used_outside_scope"></span>**WBEMMOF\_E\_QUALIFIER\_USED\_OUTSIDE\_SCOPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-706">2147762222 (0x8004402E)</span><span class="sxs-lookup"><span data-stu-id="41d1d-706">2147762222 (0x8004402E)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-707">O qualificador é usado fora de seu escopo.</span><span class="sxs-lookup"><span data-stu-id="41d1d-707">The qualifier is used outside of its scope.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-708"><span id="WBEMMOF_E_ERROR_CREATING_TEMP_FILE"></span><span id="wbemmof_e_error_creating_temp_file"></span>**WBEMMOF \_ E \_ erro \_ ao \_ criar \_ arquivo temporário**</span><span class="sxs-lookup"><span data-stu-id="41d1d-708"><span id="WBEMMOF_E_ERROR_CREATING_TEMP_FILE"></span><span id="wbemmof_e_error_creating_temp_file"></span>**WBEMMOF\_E\_ERROR\_CREATING\_TEMP\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-709">2147762223 (0x8004402F)</span><span class="sxs-lookup"><span data-stu-id="41d1d-709">2147762223 (0x8004402F)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-710">Erro ao criar arquivo temporário.</span><span class="sxs-lookup"><span data-stu-id="41d1d-710">Error creating temporary file.</span></span> <span data-ttu-id="41d1d-711">O arquivo temporário é um estágio intermediário na compilação do MOF.</span><span class="sxs-lookup"><span data-stu-id="41d1d-711">The temporary file is an intermediate stage in the MOF compilation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-712"><span id="WBEMMOF_E_ERROR_INVALID_INCLUDE_FILE"></span><span id="wbemmof_e_error_invalid_include_file"></span>**WBEMMOF \_ E \_ erro \_ de \_ inclusão inválido de \_ arquivo**</span><span class="sxs-lookup"><span data-stu-id="41d1d-712"><span id="WBEMMOF_E_ERROR_INVALID_INCLUDE_FILE"></span><span id="wbemmof_e_error_invalid_include_file"></span>**WBEMMOF\_E\_ERROR\_INVALID\_INCLUDE\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-713">2147762224 (0x80044030)</span><span class="sxs-lookup"><span data-stu-id="41d1d-713">2147762224 (0x80044030)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-714">Um arquivo incluído no MOF pelo comando de pré-processador [ \# include](-include.md) não é válido.</span><span class="sxs-lookup"><span data-stu-id="41d1d-714">A file included in the MOF by the preprocessor command [\#include](-include.md) is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41d1d-715"><span id="WBEMMOF_E_INVALID_DELETECLASS_SYNTAX"></span><span id="wbemmof_e_invalid_deleteclass_syntax"></span>**WBEMMOF \_ E \_ \_ sintaxe DELETECLASS inválida \_**</span><span class="sxs-lookup"><span data-stu-id="41d1d-715"><span id="WBEMMOF_E_INVALID_DELETECLASS_SYNTAX"></span><span id="wbemmof_e_invalid_deleteclass_syntax"></span>**WBEMMOF\_E\_INVALID\_DELETECLASS\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d1d-716">2147762225 (0x80044031)</span><span class="sxs-lookup"><span data-stu-id="41d1d-716">2147762225 (0x80044031)</span></span>
</dt> <dt>



<span data-ttu-id="41d1d-717">A sintaxe para os comandos de pré-processador [ \# pragma deleteinstance](pragma-deleteinstance.md) ou [ \# pragma DeleteClass](pragma-deleteclass.md) não é válida.</span><span class="sxs-lookup"><span data-stu-id="41d1d-717">The syntax for the preprocessor commands [\#pragma deleteinstance](pragma-deleteinstance.md) or [\#pragma deleteclass](pragma-deleteclass.md) is not valid.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="41d1d-718">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41d1d-718">Requirements</span></span>



| <span data-ttu-id="41d1d-719">Requisito</span><span class="sxs-lookup"><span data-stu-id="41d1d-719">Requirement</span></span> | <span data-ttu-id="41d1d-720">Valor</span><span class="sxs-lookup"><span data-stu-id="41d1d-720">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="41d1d-721">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="41d1d-721">Minimum supported client</span></span><br/> | <span data-ttu-id="41d1d-722">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="41d1d-722">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="41d1d-723">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="41d1d-723">Minimum supported server</span></span><br/> | <span data-ttu-id="41d1d-724">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="41d1d-724">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="41d1d-725">parâmetro</span><span class="sxs-lookup"><span data-stu-id="41d1d-725">Header</span></span><br/>                   | <dl> <span data-ttu-id="41d1d-726"><dt>WbemCli. h</dt></span><span class="sxs-lookup"><span data-stu-id="41d1d-726"><dt>WbemCli.h</dt></span></span> </dl>   |
| <span data-ttu-id="41d1d-727">INSERI</span><span class="sxs-lookup"><span data-stu-id="41d1d-727">IDL</span></span><br/>                      | <dl> <span data-ttu-id="41d1d-728"><dt>WbemCli. idl</dt></span><span class="sxs-lookup"><span data-stu-id="41d1d-728"><dt>WbemCli.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41d1d-729">Confira também</span><span class="sxs-lookup"><span data-stu-id="41d1d-729">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41d1d-730">Códigos de retorno do WMI</span><span class="sxs-lookup"><span data-stu-id="41d1d-730">WMI Return Codes</span></span>](wmi-return-codes.md)
</dt> </dl>

 

