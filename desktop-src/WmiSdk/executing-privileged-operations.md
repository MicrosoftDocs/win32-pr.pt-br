---
description: As operações privilegiadas exigem privilégios de segurança como SeLoadDriverPrivilege (wbemPrivilegeLoadDriver nas constantes da API de script), um privilégio que deve ser habilitado para uma conta que esteja carregando um driver de dispositivo.
ms.assetid: 11bb8723-f329-4083-8219-2256ce44a5e3
ms.tgt_platform: multiple
title: Executando operações privilegiadas
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 37abba9d774025825611e311f08414b50e660f65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105797674"
---
# <a name="executing-privileged-operations"></a><span data-ttu-id="d36d7-103">Executando operações privilegiadas</span><span class="sxs-lookup"><span data-stu-id="d36d7-103">Executing Privileged Operations</span></span>

<span data-ttu-id="d36d7-104">As operações privilegiadas exigem privilégios de segurança como **SeLoadDriverPrivilege** (**wbemPrivilegeLoadDriver** nas [constantes da API de script](scripting-api-constants.md)), um privilégio que deve ser habilitado para uma conta que esteja carregando um driver de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d36d7-104">Privileged operations require security privileges such as **SeLoadDriverPrivilege** (**wbemPrivilegeLoadDriver** in the [Scripting API Constants](scripting-api-constants.md)), a privilege that must be enabled for an account that is loading a device driver.</span></span> <span data-ttu-id="d36d7-105">Você não pode adicionar privilégios a um administrador ou usuário por meio do WMI, só pode habilitar os privilégios que a conta já tem.</span><span class="sxs-lookup"><span data-stu-id="d36d7-105">You cannot add privileges to an administrator or user through WMI, you can only enable privileges that the account already has.</span></span> <span data-ttu-id="d36d7-106">Para obter uma lista de privilégios, [**consulte \_ constantes de privilégio**](privilege-constants.md).</span><span class="sxs-lookup"><span data-stu-id="d36d7-106">For a list of privileges, see [**Privilege\_Constants**](privilege-constants.md).</span></span>

<span data-ttu-id="d36d7-107">Por padrão, um usuário local em um computador pode ler dados estáticos do [*repositório do WMI*](gloss-w.md), gravar em instâncias fornecidas por provedores e executar métodos de provedor, a menos que o provedor aplique requisitos de segurança especiais próprios.</span><span class="sxs-lookup"><span data-stu-id="d36d7-107">By default, a local user on a computer can read static data from the [*WMI repository*](gloss-w.md), write to instances supplied by providers, and execute provider methods, unless the provider enforces special security requirements of its own.</span></span> <span data-ttu-id="d36d7-108">Somente os administradores podem [se conectar a um computador remoto](connecting-to-wmi-on-a-remote-computer.md), alterar descritores de segurança ou alterar dados estáticos do repositório WMI, como uma definição de classe WMI.</span><span class="sxs-lookup"><span data-stu-id="d36d7-108">Only administrators can [connect to a remote computer](connecting-to-wmi-on-a-remote-computer.md), change security descriptors, or change static WMI repository data, such as a WMI class definition.</span></span> <span data-ttu-id="d36d7-109">Todos os privilégios estão habilitados para uma conexão remota.</span><span class="sxs-lookup"><span data-stu-id="d36d7-109">All privileges are enabled for a remote connection.</span></span> <span data-ttu-id="d36d7-110">Para obter mais informações, consulte [protegendo uma conexão WMI remota](securing-a-remote-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="d36d7-110">For more information, see [Securing a Remote WMI Connection](securing-a-remote-wmi-connection.md).</span></span>

<span data-ttu-id="d36d7-111">As constantes de privilégio para C++ diferem das que são usadas por linguagens de automação, como Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="d36d7-111">The privilege constants for C++ differ from those that are used by automation languages such as Visual Basic.</span></span> <span data-ttu-id="d36d7-112">Os scripts devem usar o valor da constante em vez do nome.</span><span class="sxs-lookup"><span data-stu-id="d36d7-112">Scripts must use the value of the constant rather than the name.</span></span> <span data-ttu-id="d36d7-113">Para obter mais informações, consulte [executando operações privilegiadas usando C++](executing-privileged-operations-using-c-.md) ou [executando operações privilegiadas usando o VBScript](executing-privileged-operations-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="d36d7-113">For more information, see [Executing Privileged Operations Using C++](executing-privileged-operations-using-c-.md) or [Executing Privileged Operations Using VBScript](executing-privileged-operations-using-vbscript.md).</span></span>

<span data-ttu-id="d36d7-114">Uma causa comum de erros de acesso negado ao usar o WMI é a falta de um privilégio habilitado para operações, como obter todas as instâncias do [**Win32 \_ NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d36d7-114">A common cause of access denied errors when using WMI is the lack of an enabled privilege for operations, such as getting all instances of [**Win32\_NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)).</span></span> <span data-ttu-id="d36d7-115">Sem habilitar o privilégio **SeSecurity** , você não pode acessar o arquivo de log de segurança.</span><span class="sxs-lookup"><span data-stu-id="d36d7-115">Without enabling the **SeSecurity** privilege, you cannot access the Security log file.</span></span>

<span data-ttu-id="d36d7-116">O exemplo de código VBScript a seguir mostra como definir o privilégio **SeSecurity** na cadeia de caracteres do moniker.</span><span class="sxs-lookup"><span data-stu-id="d36d7-116">The following VBScript code example shows how to set the **SeSecurity** privilege in the moniker string.</span></span> <span data-ttu-id="d36d7-117">Quando usado no moniker, o nome do privilégio entre parênteses descarta o "se" inicial.</span><span class="sxs-lookup"><span data-stu-id="d36d7-117">When used in the moniker, the privilege name in parentheses drops the initial "Se".</span></span> <span data-ttu-id="d36d7-118">Para obter mais informações, consulte [construindo uma cadeia de caracteres de moniker](constructing-a-moniker-string.md).</span><span class="sxs-lookup"><span data-stu-id="d36d7-118">For more information, see [Constructing a Moniker String](constructing-a-moniker-string.md).</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate,(Security)}!\\" _
    & strComputer & "\root\cimv2")
Set colFiles = objWMIService.ExecQuery _
    ("Select * from Win32_NTEventLogFile " _
    & "Where LogFileName='Security'")
For Each LogFile in colFiles
Wscript.Echo LogFile.NumberOfRecords
Next
```



## <a name="related-topics"></a><span data-ttu-id="d36d7-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d36d7-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d36d7-120">**Constantes de privilégio**</span><span class="sxs-lookup"><span data-stu-id="d36d7-120">**Privilege Constants**</span></span>](privilege-constants.md)
</dt> </dl>

 

 
