---
title: Método TaskService. Connect
description: Para scripts, o se conecta a um computador remoto e associa todas as chamadas subsequentes nessa interface a uma sessão remota.
ms.assetid: 206087df-307c-4ba9-9e83-915f5287f281
keywords:
- Agendador de Tarefas do método Connect
- Método Connect Agendador de Tarefas, objeto TaskService
- Agendador de Tarefas de objeto TaskService, método Connect
topic_type:
- apiref
api_name:
- TaskService.Connect
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1db5f13e20da825cbdaf45ae399279687f6ff4aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918212"
---
# <a name="taskserviceconnect-method"></a><span data-ttu-id="c1b17-106">Método TaskService. Connect</span><span class="sxs-lookup"><span data-stu-id="c1b17-106">TaskService.Connect method</span></span>

<span data-ttu-id="c1b17-107">Para scripts, o se conecta a um computador remoto e associa todas as chamadas subsequentes nessa interface a uma sessão remota.</span><span class="sxs-lookup"><span data-stu-id="c1b17-107">For scripting, connects to a remote machine and associates all subsequent calls on this interface with a remote session.</span></span> <span data-ttu-id="c1b17-108">Se o parâmetro ServerName estiver vazio, esse método será executado no computador local.</span><span class="sxs-lookup"><span data-stu-id="c1b17-108">If the serverName parameter is empty, then this method will execute on the local computer.</span></span> <span data-ttu-id="c1b17-109">Se a userId não for especificada, o token atual será usado.</span><span class="sxs-lookup"><span data-stu-id="c1b17-109">If the userId is not specified, then the current token is used.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1b17-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c1b17-110">Syntax</span></span>


```VB
TaskService.Connect( _
  [ ByVal serverName ], _
  [ ByVal user ], _
  [ ByVal domain ], _
  [ ByVal password ] _
)
```



## <a name="parameters"></a><span data-ttu-id="c1b17-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c1b17-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1b17-112">*nome do Server* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="c1b17-112">*serverName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c1b17-113">O nome do computador ao qual você deseja se conectar.</span><span class="sxs-lookup"><span data-stu-id="c1b17-113">The name of the computer that you want to connect to.</span></span> <span data-ttu-id="c1b17-114">Se o parâmetro ServerName estiver vazio, esse método será executado no computador local.</span><span class="sxs-lookup"><span data-stu-id="c1b17-114">If the serverName parameter is empty, then this method will execute on the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="c1b17-115">*usuário* \[ do em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="c1b17-115">*user* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c1b17-116">O nome de usuário que é usado durante a conexão com o computador.</span><span class="sxs-lookup"><span data-stu-id="c1b17-116">The user name that is used during the connection to the computer.</span></span> <span data-ttu-id="c1b17-117">Se o usuário não for especificado, o token atual será usado.</span><span class="sxs-lookup"><span data-stu-id="c1b17-117">If the user is not specified, then the current token is used.</span></span>

</dd> <dt>

<span data-ttu-id="c1b17-118">*domínio* \[ do em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="c1b17-118">*domain* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c1b17-119">O domínio do usuário especificado no parâmetro *User* .</span><span class="sxs-lookup"><span data-stu-id="c1b17-119">The domain of the user specified in the *user* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="c1b17-120">*senha* \[ do em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="c1b17-120">*password* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c1b17-121">A senha usada para se conectar ao computador.</span><span class="sxs-lookup"><span data-stu-id="c1b17-121">The password that is used to connect to the computer.</span></span> <span data-ttu-id="c1b17-122">Se o nome de usuário e a senha não forem especificados, o token atual será usado.</span><span class="sxs-lookup"><span data-stu-id="c1b17-122">If the user name and password are not specified, then the current token is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1b17-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c1b17-123">Return value</span></span>

<span data-ttu-id="c1b17-124">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="c1b17-124">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1b17-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="c1b17-125">Remarks</span></span>

<span data-ttu-id="c1b17-126">O método **TaskService. Connect** deve ser chamado antes de chamar qualquer um dos outros métodos [**TaskService**](taskservice.md) .</span><span class="sxs-lookup"><span data-stu-id="c1b17-126">The **TaskService.Connect** method should be called before calling any of the other [**TaskService**](taskservice.md) methods.</span></span>

<span data-ttu-id="c1b17-127">Se o método Connect falhar, você poderá coletar o identificador de erro para localizar o significado do erro.</span><span class="sxs-lookup"><span data-stu-id="c1b17-127">If the Connect method fails, you can collect the error identifier to find the meaning of the error.</span></span> <span data-ttu-id="c1b17-128">A tabela a seguir lista os identificadores de erro e suas descrições.</span><span class="sxs-lookup"><span data-stu-id="c1b17-128">The following table lists the error identifiers and their descriptions.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c1b17-129">Identificador de erro</span><span class="sxs-lookup"><span data-stu-id="c1b17-129">Error Identifier</span></span></th>
<th><span data-ttu-id="c1b17-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1b17-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c1b17-131">0x80070005</span><span class="sxs-lookup"><span data-stu-id="c1b17-131">0x80070005</span></span></td>
<td><span data-ttu-id="c1b17-132">Acesso negado para se conectar ao serviço de Agendador de Tarefas.</span><span class="sxs-lookup"><span data-stu-id="c1b17-132">Access is denied to connect to the Task Scheduler service.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c1b17-133">0x80041315</span><span class="sxs-lookup"><span data-stu-id="c1b17-133">0x80041315</span></span></td>
<td><span data-ttu-id="c1b17-134">O serviço de Agendador de Tarefas não está em execução.</span><span class="sxs-lookup"><span data-stu-id="c1b17-134">The Task Scheduler service is not running.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c1b17-135">0x8007000e</span><span class="sxs-lookup"><span data-stu-id="c1b17-135">0x8007000e</span></span></td>
<td><span data-ttu-id="c1b17-136">O aplicativo não tem memória suficiente para concluir a operação ou o <em>usuário</em>, a <em>senha</em>ou o <em>domínio</em> tem pelo menos um valor nulo e um não nulo.</span><span class="sxs-lookup"><span data-stu-id="c1b17-136">The application does not have enough memory to complete the operation or the <em>user</em>, <em>password</em>, or <em>domain</em> has at least one null and one non-null value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c1b17-137">53</span><span class="sxs-lookup"><span data-stu-id="c1b17-137">53</span></span></td>
<td><span data-ttu-id="c1b17-138">Esse erro é retornado nas seguintes situações:</span><span class="sxs-lookup"><span data-stu-id="c1b17-138">This error is returned in the following situations:</span></span>
<ul>
<li><span data-ttu-id="c1b17-139">O nome do computador especificado no parâmetro <em>ServerName</em> não existe.</span><span class="sxs-lookup"><span data-stu-id="c1b17-139">The computer name specified in the <em>serverName</em> parameter does not exist.</span></span></li>
<li><span data-ttu-id="c1b17-140">Quando você está tentando se conectar a um computador com Windows Server 2003 ou Windows XP, o computador remoto não tem a exceção de firewall de compartilhamento de arquivos e impressoras habilitada ou o serviço de registro remoto não está em execução.</span><span class="sxs-lookup"><span data-stu-id="c1b17-140">When you are trying to connect to a Windows Server 2003 or Windows XP computer, and the remote computer does not have the File and Printer Sharing firewall exception enabled or the Remote Registry service is not running.</span></span></li>
<li><span data-ttu-id="c1b17-141">Quando você estiver tentando se conectar a um computador com Windows Vista e o computador remoto não tiver a exceção de firewall de gerenciamento de tarefas agendadas remotas habilitada e a exceção de firewall de compartilhamento de arquivos e impressoras estiver habilitada ou o serviço de registro remoto não estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="c1b17-141">When you are trying to connect to a Windows Vista computer, and the remote computer does not have the Remote Scheduled Tasks Management firewall exception enabled and the File and Printer Sharing firewall exception enabled, or the Remote Registry service is not running.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c1b17-142">50</span><span class="sxs-lookup"><span data-stu-id="c1b17-142">50</span></span></td>
<td><span data-ttu-id="c1b17-143">Os parâmetros de <em>usuário</em>, <em>senha</em>ou <em>domínio</em> não podem ser especificados ao se conectar a um computador remoto com Windows XP ou Windows Server 2003 de um computador com Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c1b17-143">The <em>user</em>, <em>password</em>, or <em>domain</em> parameters cannot be specified when connecting to a remote Windows XP or Windows Server 2003 computer from a Windows Vista computer.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="c1b17-144">Se você estiver se conectando a um computador remoto com Windows Vista de um Windows Vista, será necessário permitir a exceção de firewall de gerenciamento de tarefas agendadas remotas no computador remoto.</span><span class="sxs-lookup"><span data-stu-id="c1b17-144">If you are to connecting to a remote Windows Vista computer from a Windows Vista, you need to allow the Remote Scheduled Tasks Management firewall exception on the remote computer.</span></span> <span data-ttu-id="c1b17-145">Para permitir essa exceção, clique em Iniciar, painel de controle, segurança, permitir um programa pelo firewall do Windows e marque a caixa de seleção gerenciamento remoto de tarefas agendadas.</span><span class="sxs-lookup"><span data-stu-id="c1b17-145">To allow this exception click Start, Control Panel, Security, Allow a program through Windows Firewall, and then select the Remote Scheduled Tasks Management check box.</span></span> <span data-ttu-id="c1b17-146">Em seguida, clique no botão OK na caixa de diálogo Configurações do firewall do Windows.</span><span class="sxs-lookup"><span data-stu-id="c1b17-146">Then click the Ok button in the Windows Firewall Settings dialog box.</span></span>

<span data-ttu-id="c1b17-147">Se você estiver se conectando a um computador remoto com Windows XP ou Windows Server 2003 de um computador com Windows Vista, será necessário permitir a exceção de firewall de compartilhamento de arquivos e impressoras no computador remoto.</span><span class="sxs-lookup"><span data-stu-id="c1b17-147">If you are connecting to a remote Windows XP or Windows Server 2003 computer from a Windows Vista computer, you need to allow the File and Printer Sharing firewall exception on the remote computer.</span></span> <span data-ttu-id="c1b17-148">Para permitir essa exceção, clique em Iniciar, painel de controle, clique duas vezes em Firewall do Windows, selecione a guia exceções e selecione a exceção de firewall de compartilhamento de arquivos e impressoras.</span><span class="sxs-lookup"><span data-stu-id="c1b17-148">To allow this exception click Start, Control Panel, double-click Windows Firewall, select the Exceptions tab, and then select the File and Printer Sharing firewall exception.</span></span> <span data-ttu-id="c1b17-149">Em seguida, clique no botão OK na caixa de diálogo Firewall do Windows.</span><span class="sxs-lookup"><span data-stu-id="c1b17-149">Then click the OK button in the Windows Firewall dialog box.</span></span> <span data-ttu-id="c1b17-150">O serviço registro remoto também deve estar em execução no computador remoto.</span><span class="sxs-lookup"><span data-stu-id="c1b17-150">The Remote Registry service must also be running on the remote computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1b17-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1b17-151">Requirements</span></span>



| <span data-ttu-id="c1b17-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1b17-152">Requirement</span></span> | <span data-ttu-id="c1b17-153">Valor</span><span class="sxs-lookup"><span data-stu-id="c1b17-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1b17-154">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c1b17-154">Minimum supported client</span></span><br/> | <span data-ttu-id="c1b17-155">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c1b17-155">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="c1b17-156">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c1b17-156">Minimum supported server</span></span><br/> | <span data-ttu-id="c1b17-157">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c1b17-157">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c1b17-158">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="c1b17-158">Type library</span></span><br/>             | <dl> <span data-ttu-id="c1b17-159"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c1b17-159"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c1b17-160">DLL</span><span class="sxs-lookup"><span data-stu-id="c1b17-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1b17-161"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1b17-161"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





