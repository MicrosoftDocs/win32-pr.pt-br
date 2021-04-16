---
title: Enumeração ExtendedDisconnectReasonCode
description: Define informações estendidas sobre o motivo do controle para desconexão.
ms.assetid: E73E73B4-6C6B-4270-A1BD-947FA6D7B31B
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de enumeração ExtendedDisconnectReasonCode
topic_type:
- apiref
api_name:
- ExtendedDisconnectReasonCode
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 657d0faee03ca37b9a5a49b95b978a24b0c8955c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105779429"
---
# <a name="extendeddisconnectreasoncode-enumeration"></a><span data-ttu-id="d3896-104">Enumeração ExtendedDisconnectReasonCode</span><span class="sxs-lookup"><span data-stu-id="d3896-104">ExtendedDisconnectReasonCode enumeration</span></span>

<span data-ttu-id="d3896-105">Define informações estendidas sobre o motivo do controle para desconexão.</span><span class="sxs-lookup"><span data-stu-id="d3896-105">Defines extended information about the control's reason for disconnection.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3896-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d3896-106">Syntax</span></span>


```C++
typedef enum _ExtendedDisconnectReasonCode { 
  exDiscReasonNoInfo                            = 0,
  exDiscReasonAPIInitiatedDisconnect            = 1,
  exDiscReasonAPIInitiatedLogoff                = 2,
  exDiscReasonServerIdleTimeout                 = 3,
  exDiscReasonServerLogonTimeout                = 4,
  exDiscReasonReplacedByOtherConnection         = 5,
  exDiscReasonOutOfMemory                       = 6,
  exDiscReasonServerDeniedConnection            = 7,
  exDiscReasonServerDeniedConnectionFips        = 8,
  exDiscReasonServerInsufficientPrivileges      = 9,
  exDiscReasonServerFreshCredsRequired          = 10,
  exDiscReasonRpcInitiatedDisconnectByUser      = 11,
  exDiscReasonLogoffByUser                      = 2,
  exDiscReasonLicenseInternal                   = 256,
  exDiscReasonLicenseNoLicenseServer            = 257,
  exDiscReasonLicenseNoLicense                  = 258,
  exDiscReasonLicenseErrClientMsg               = 259,
  exDiscReasonLicenseHwidDoesntMatchLicense     = 260,
  exDiscReasonLicenseErrClientLicense           = 261,
  exDiscReasonLicenseCantFinishProtocol         = 262,
  exDiscReasonLicenseClientEndedProtocol        = 263,
  exDiscReasonLicenseErrClientEncryption        = 264,
  exDiscReasonLicenseCantUpgradeLicense         = 265,
  exDiscReasonLicenseNoRemoteConnections        = 266,
  exDiscReasonLicenseCreatingLicStoreAccDenied  = 267,
  exDiscReasonRdpEncInvalidCredentials          = 768,
  exDiscReasonProtocolRangeStart                = 4096,
  exDiscReasonProtocolRangeEnd                  = 32767
} ExtendedDisconnectReasonCode;
```



## <a name="constants"></a><span data-ttu-id="d3896-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="d3896-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d3896-108"><span id="exDiscReasonNoInfo"></span><span id="exdiscreasonnoinfo"></span><span id="EXDISCREASONNOINFO"></span>**exDiscReasonNoInfo**</span><span class="sxs-lookup"><span data-stu-id="d3896-108"><span id="exDiscReasonNoInfo"></span><span id="exdiscreasonnoinfo"></span><span id="EXDISCREASONNOINFO"></span>**exDiscReasonNoInfo**</span></span>
</dt> <dd>

<span data-ttu-id="d3896-109">Não há informações adicionais disponíveis.</span><span class="sxs-lookup"><span data-stu-id="d3896-109">No additional information is available.</span></span>

</dd> <dt>

<span data-ttu-id="d3896-110"><span id="exDiscReasonAPIInitiatedDisconnect"></span><span id="exdiscreasonapiinitiateddisconnect"></span><span id="EXDISCREASONAPIINITIATEDDISCONNECT"></span>**exDiscReasonAPIInitiatedDisconnect**</span><span class="sxs-lookup"><span data-stu-id="d3896-110"><span id="exDiscReasonAPIInitiatedDisconnect"></span><span id="exdiscreasonapiinitiateddisconnect"></span><span id="EXDISCREASONAPIINITIATEDDISCONNECT"></span>**exDiscReasonAPIInitiatedDisconnect**</span></span>
</dt> <dd>

<span data-ttu-id="d3896-111">Um aplicativo iniciou a desconexão.</span><span class="sxs-lookup"><span data-stu-id="d3896-111">An application initiated the disconnection.</span></span>

</dd> <dt>

<span data-ttu-id="d3896-112"><span id="exDiscReasonAPIInitiatedLogoff"></span><span id="exdiscreasonapiinitiatedlogoff"></span><span id="EXDISCREASONAPIINITIATEDLOGOFF"></span>**exDiscReasonAPIInitiatedLogoff**</span><span class="sxs-lookup"><span data-stu-id="d3896-112"><span id="exDiscReasonAPIInitiatedLogoff"></span><span id="exdiscreasonapiinitiatedlogoff"></span><span id="EXDISCREASONAPIINITIATEDLOGOFF"></span>**exDiscReasonAPIInitiatedLogoff**</span></span>
</dt> <dd>

<span data-ttu-id="d3896-113">Um aplicativo fez logoff do cliente.</span><span class="sxs-lookup"><span data-stu-id="d3896-113">An application logged off the client.</span></span>

</dd> <dt>

<span data-ttu-id="d3896-114"><span id="exDiscReasonServerIdleTimeout"></span><span id="exdiscreasonserveridletimeout"></span><span id="EXDISCREASONSERVERIDLETIMEOUT"></span>**exDiscReasonServerIdleTimeout**</span><span class="sxs-lookup"><span data-stu-id="d3896-114"><span id="exDiscReasonServerIdleTimeout"></span><span id="exdiscreasonserveridletimeout"></span><span id="EXDISCREASONSERVERIDLETIMEOUT"></span>**exDiscReasonServerIdleTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="d3896-115">O servidor desconectou o cliente porque o cliente esteve ocioso por um período de tempo maior do que o período de tempo limite designado.</span><span class="sxs-lookup"><span data-stu-id="d3896-115">The server has disconnected the client because the client has been idle for a period of time longer than the designated time-out period.</span></span>

</dd> <dt>

<span data-ttu-id="d3896-116"><span id="exDiscReasonServerLogonTimeout"></span><span id="exdiscreasonserverlogontimeout"></span><span id="EXDISCREASONSERVERLOGONTIMEOUT"></span>**exDiscReasonServerLogonTimeout**</span><span class="sxs-lookup"><span data-stu-id="d3896-116"><span id="exDiscReasonServerLogonTimeout"></span><span id="exdiscreasonserverlogontimeout"></span><span id="EXDISCREASONSERVERLOGONTIMEOUT"></span>**exDiscReasonServerLogonTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="d3896-117">O servidor desconectou o cliente porque o cliente excedeu o período designado para conexão.</span><span class="sxs-lookup"><span data-stu-id="d3896-117">The server has disconnected the client because the client has exceeded the period designated for connection.</span></span>

</dd> <dt>

<span data-ttu-id="d3896-118"><span id="exDiscReasonReplacedByOtherConnection"></span><span id="exdiscreasonreplacedbyotherconnection"></span><span id="EXDISCREASONREPLACEDBYOTHERCONNECTION"></span>**exDiscReasonReplacedByOtherConnection**</span><span class="sxs-lookup"><span data-stu-id="d3896-118"><span id="exDiscReasonReplacedByOtherConnection"></span><span id="exdiscreasonreplacedbyotherconnection"></span><span id="EXDISCREASONREPLACEDBYOTHERCONNECTION"></span>**exDiscReasonReplacedByOtherConnection**</span></span>
</dt> <dd>

<span data-ttu-id="d3896-119">A conexão do cliente foi substituída por outra conexão.</span><span class="sxs-lookup"><span data-stu-id="d3896-119">The client's connection was replaced by another connection.</span></span>

</dd> <dt>

<span data-ttu-id="d3896-120"><span id="exDiscReasonOutOfMemory"></span><span id="exdiscreasonoutofmemory"></span><span id="EXDISCREASONOUTOFMEMORY"></span>**exDiscReasonOutOfMemory**</span><span class="sxs-lookup"><span data-stu-id="d3896-120"><span id="exDiscReasonOutOfMemory"></span><span id="exdiscreasonoutofmemory"></span><span id="EXDISCREASONOUTOFMEMORY"></span>**exDiscReasonOutOfMemory**</span></span>
</dt> <dd>

<span data-ttu-id="d3896-121">Não há memória disponível.</span><span class="sxs-lookup"><span data-stu-id="d3896-121">No memory is available.</span></span>

</dd> <dt>

<span data-ttu-id="d3896-122"><span id="exDiscReasonServerDeniedConnection"></span><span id="exdiscreasonserverdeniedconnection"></span><span id="EXDISCREASONSERVERDENIEDCONNECTION"></span>**exDiscReasonServerDeniedConnection**</span><span class="sxs-lookup"><span data-stu-id="d3896-122"><span id="exDiscReasonServerDeniedConnection"></span><span id="exdiscreasonserverdeniedconnection"></span><span id="EXDISCREASONSERVERDENIEDCONNECTION"></span>**exDiscReasonServerDeniedConnection**</span></span>
</dt> <dd>

<span data-ttu-id="d3896-123">O servidor negou a conexão.</span><span class="sxs-lookup"><span data-stu-id="d3896-123">The server denied the connection.</span></span>

</dd> <dt>

<span data-ttu-id="d3896-124"><span id="exDiscReasonServerDeniedConnectionFips"></span><span id="exdiscreasonserverdeniedconnectionfips"></span><span id="EXDISCREASONSERVERDENIEDCONNECTIONFIPS"></span>**exDiscReasonServerDeniedConnectionFips**</span><span class="sxs-lookup"><span data-stu-id="d3896-124"><span id="exDiscReasonServerDeniedConnectionFips"></span><span id="exdiscreasonserverdeniedconnectionfips"></span><span id="EXDISCREASONSERVERDENIEDCONNECTIONFIPS"></span>**exDiscReasonServerDeniedConnectionFips**</span></span>
</dt> <dd>

<span data-ttu-id="d3896-125">O servidor negou a conexão por motivos de segurança.</span><span class="sxs-lookup"><span data-stu-id="d3896-125">The server denied the connection for security reasons.</span></span>

</dd> <dt>

<span data-ttu-id="d3896-126"><span id="exDiscReasonServerInsufficientPrivileges"></span><span id="exdiscreasonserverinsufficientprivileges"></span><span id="EXDISCREASONSERVERINSUFFICIENTPRIVILEGES"></span>**exDiscReasonServerInsufficientPrivileges**</span><span class="sxs-lookup"><span data-stu-id="d3896-126"><span id="exDiscReasonServerInsufficientPrivileges"></span><span id="exdiscreasonserverinsufficientprivileges"></span><span id="EXDISCREASONSERVERINSUFFICIENTPRIVILEGES"></span>**exDiscReasonServerInsufficientPrivileges**</span></span>
</dt> <dd>

<span data-ttu-id="d3896-127">O servidor negou a conexão por motivos de segurança.</span><span class="sxs-lookup"><span data-stu-id="d3896-127">The server denied the connection for security reasons.</span></span>

</dd> <dt>

<span data-ttu-id="d3896-128"><span id="exDiscReasonServerFreshCredsRequired"></span><span id="exdiscreasonserverfreshcredsrequired"></span><span id="EXDISCREASONSERVERFRESHCREDSREQUIRED"></span>**exDiscReasonServerFreshCredsRequired**</span><span class="sxs-lookup"><span data-stu-id="d3896-128"><span id="exDiscReasonServerFreshCredsRequired"></span><span id="exdiscreasonserverfreshcredsrequired"></span><span id="EXDISCREASONSERVERFRESHCREDSREQUIRED"></span>**exDiscReasonServerFreshCredsRequired**</span></span>
</dt> <dd>

<span data-ttu-id="d3896-129">As novas credenciais são necessárias.</span><span class="sxs-lookup"><span data-stu-id="d3896-129">Fresh credentials are required.</span></span>

</dd> <dt>

<span data-ttu-id="d3896-130"><span id="exDiscReasonRpcInitiatedDisconnectByUser"></span><span id="exdiscreasonrpcinitiateddisconnectbyuser"></span><span id="EXDISCREASONRPCINITIATEDDISCONNECTBYUSER"></span>**exDiscReasonRpcInitiatedDisconnectByUser**</span><span class="sxs-lookup"><span data-stu-id="d3896-130"><span id="exDiscReasonRpcInitiatedDisconnectByUser"></span><span id="exdiscreasonrpcinitiateddisconnectbyuser"></span><span id="EXDISCREASONRPCINITIATEDDISCONNECTBYUSER"></span>**exDiscReasonRpcInitiatedDisconnectByUser**</span></span>
</dt> <dd>

<span data-ttu-id="d3896-131">A atividade do usuário iniciou a desconexão.</span><span class="sxs-lookup"><span data-stu-id="d3896-131">User activity has initiated the disconnect.</span></span>

</dd> <dt>

<span data-ttu-id="d3896-132"><span id="exDiscReasonLogoffByUser"></span><span id="exdiscreasonlogoffbyuser"></span><span id="EXDISCREASONLOGOFFBYUSER"></span>**exDiscReasonLogoffByUser**</span><span class="sxs-lookup"><span data-stu-id="d3896-132"><span id="exDiscReasonLogoffByUser"></span><span id="exdiscreasonlogoffbyuser"></span><span id="EXDISCREASONLOGOFFBYUSER"></span>**exDiscReasonLogoffByUser**</span></span>
</dt> <dd>

<span data-ttu-id="d3896-133">O usuário fez logoff, desconectando a sessão.</span><span class="sxs-lookup"><span data-stu-id="d3896-133">The user logged off, disconnecting the session.</span></span>

</dd> <dt>

<span data-ttu-id="d3896-134"><span id="exDiscReasonLicenseInternal"></span><span id="exdiscreasonlicenseinternal"></span><span id="EXDISCREASONLICENSEINTERNAL"></span>**exDiscReasonLicenseInternal**</span><span class="sxs-lookup"><span data-stu-id="d3896-134"><span id="exDiscReasonLicenseInternal"></span><span id="exdiscreasonlicenseinternal"></span><span id="EXDISCREASONLICENSEINTERNAL"></span>**exDiscReasonLicenseInternal**</span></span>
</dt> <dd>

<span data-ttu-id="d3896-135">Erro interno de licenciamento.</span><span class="sxs-lookup"><span data-stu-id="d3896-135">Internal licensing error.</span></span>

</dd> <dt>

<span data-ttu-id="d3896-136"><span id="exDiscReasonLicenseNoLicenseServer"></span><span id="exdiscreasonlicensenolicenseserver"></span><span id="EXDISCREASONLICENSENOLICENSESERVER"></span>**exDiscReasonLicenseNoLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="d3896-136"><span id="exDiscReasonLicenseNoLicenseServer"></span><span id="exdiscreasonlicensenolicenseserver"></span><span id="EXDISCREASONLICENSENOLICENSESERVER"></span>**exDiscReasonLicenseNoLicenseServer**</span></span>
</dt> <dd>

<span data-ttu-id="d3896-137">Nenhum servidor de licença estava disponível.</span><span class="sxs-lookup"><span data-stu-id="d3896-137">No license server was available.</span></span>

</dd> <dt>

<span data-ttu-id="d3896-138"><span id="exDiscReasonLicenseNoLicense"></span><span id="exdiscreasonlicensenolicense"></span><span id="EXDISCREASONLICENSENOLICENSE"></span>**exDiscReasonLicenseNoLicense**</span><span class="sxs-lookup"><span data-stu-id="d3896-138"><span id="exDiscReasonLicenseNoLicense"></span><span id="exdiscreasonlicensenolicense"></span><span id="EXDISCREASONLICENSENOLICENSE"></span>**exDiscReasonLicenseNoLicense**</span></span>
</dt> <dd>

<span data-ttu-id="d3896-139">Nenhuma licença de software válida estava disponível.</span><span class="sxs-lookup"><span data-stu-id="d3896-139">No valid software license was available.</span></span>

</dd> <dt>

<span data-ttu-id="d3896-140"><span id="exDiscReasonLicenseErrClientMsg"></span><span id="exdiscreasonlicenseerrclientmsg"></span><span id="EXDISCREASONLICENSEERRCLIENTMSG"></span>**exDiscReasonLicenseErrClientMsg**</span><span class="sxs-lookup"><span data-stu-id="d3896-140"><span id="exDiscReasonLicenseErrClientMsg"></span><span id="exdiscreasonlicenseerrclientmsg"></span><span id="EXDISCREASONLICENSEERRCLIENTMSG"></span>**exDiscReasonLicenseErrClientMsg**</span></span>
</dt> <dd>

<span data-ttu-id="d3896-141">O computador remoto recebeu uma mensagem de licenciamento que não era válida.</span><span class="sxs-lookup"><span data-stu-id="d3896-141">The remote computer received a licensing message that was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="d3896-142"><span id="exDiscReasonLicenseHwidDoesntMatchLicense"></span><span id="exdiscreasonlicensehwiddoesntmatchlicense"></span><span id="EXDISCREASONLICENSEHWIDDOESNTMATCHLICENSE"></span>**exDiscReasonLicenseHwidDoesntMatchLicense**</span><span class="sxs-lookup"><span data-stu-id="d3896-142"><span id="exDiscReasonLicenseHwidDoesntMatchLicense"></span><span id="exdiscreasonlicensehwiddoesntmatchlicense"></span><span id="EXDISCREASONLICENSEHWIDDOESNTMATCHLICENSE"></span>**exDiscReasonLicenseHwidDoesntMatchLicense**</span></span>
</dt> <dd>

<span data-ttu-id="d3896-143">A ID de hardware não corresponde à que foi designada na licença de software.</span><span class="sxs-lookup"><span data-stu-id="d3896-143">The hardware ID does not match the one designated on the software license.</span></span>

</dd> <dt>

<span data-ttu-id="d3896-144"><span id="exDiscReasonLicenseErrClientLicense"></span><span id="exdiscreasonlicenseerrclientlicense"></span><span id="EXDISCREASONLICENSEERRCLIENTLICENSE"></span>**exDiscReasonLicenseErrClientLicense**</span><span class="sxs-lookup"><span data-stu-id="d3896-144"><span id="exDiscReasonLicenseErrClientLicense"></span><span id="exdiscreasonlicenseerrclientlicense"></span><span id="EXDISCREASONLICENSEERRCLIENTLICENSE"></span>**exDiscReasonLicenseErrClientLicense**</span></span>
</dt> <dd>

<span data-ttu-id="d3896-145">Erro de licença de cliente.</span><span class="sxs-lookup"><span data-stu-id="d3896-145">Client license error.</span></span>

</dd> <dt>

<span data-ttu-id="d3896-146"><span id="exDiscReasonLicenseCantFinishProtocol"></span><span id="exdiscreasonlicensecantfinishprotocol"></span><span id="EXDISCREASONLICENSECANTFINISHPROTOCOL"></span>**exDiscReasonLicenseCantFinishProtocol**</span><span class="sxs-lookup"><span data-stu-id="d3896-146"><span id="exDiscReasonLicenseCantFinishProtocol"></span><span id="exdiscreasonlicensecantfinishprotocol"></span><span id="EXDISCREASONLICENSECANTFINISHPROTOCOL"></span>**exDiscReasonLicenseCantFinishProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="d3896-147">Problemas de rede ocorreram durante o protocolo de licenciamento.</span><span class="sxs-lookup"><span data-stu-id="d3896-147">Network problems occurred during the licensing protocol.</span></span>

</dd> <dt>

<span data-ttu-id="d3896-148"><span id="exDiscReasonLicenseClientEndedProtocol"></span><span id="exdiscreasonlicenseclientendedprotocol"></span><span id="EXDISCREASONLICENSECLIENTENDEDPROTOCOL"></span>**exDiscReasonLicenseClientEndedProtocol**</span><span class="sxs-lookup"><span data-stu-id="d3896-148"><span id="exDiscReasonLicenseClientEndedProtocol"></span><span id="exdiscreasonlicenseclientendedprotocol"></span><span id="EXDISCREASONLICENSECLIENTENDEDPROTOCOL"></span>**exDiscReasonLicenseClientEndedProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="d3896-149">O cliente encerrou o protocolo de licenciamento prematuramente.</span><span class="sxs-lookup"><span data-stu-id="d3896-149">The client ended the licensing protocol prematurely.</span></span>

</dd> <dt>

<span data-ttu-id="d3896-150"><span id="exDiscReasonLicenseErrClientEncryption"></span><span id="exdiscreasonlicenseerrclientencryption"></span><span id="EXDISCREASONLICENSEERRCLIENTENCRYPTION"></span>**exDiscReasonLicenseErrClientEncryption**</span><span class="sxs-lookup"><span data-stu-id="d3896-150"><span id="exDiscReasonLicenseErrClientEncryption"></span><span id="exdiscreasonlicenseerrclientencryption"></span><span id="EXDISCREASONLICENSEERRCLIENTENCRYPTION"></span>**exDiscReasonLicenseErrClientEncryption**</span></span>
</dt> <dd>

<span data-ttu-id="d3896-151">Uma mensagem de licenciamento foi criptografada incorretamente.</span><span class="sxs-lookup"><span data-stu-id="d3896-151">A licensing message was encrypted incorrectly.</span></span>

</dd> <dt>

<span data-ttu-id="d3896-152"><span id="exDiscReasonLicenseCantUpgradeLicense"></span><span id="exdiscreasonlicensecantupgradelicense"></span><span id="EXDISCREASONLICENSECANTUPGRADELICENSE"></span>**exDiscReasonLicenseCantUpgradeLicense**</span><span class="sxs-lookup"><span data-stu-id="d3896-152"><span id="exDiscReasonLicenseCantUpgradeLicense"></span><span id="exdiscreasonlicensecantupgradelicense"></span><span id="EXDISCREASONLICENSECANTUPGRADELICENSE"></span>**exDiscReasonLicenseCantUpgradeLicense**</span></span>
</dt> <dd>

<span data-ttu-id="d3896-153">A licença de acesso para cliente do computador local não pôde ser atualizada ou renovada.</span><span class="sxs-lookup"><span data-stu-id="d3896-153">The local computer's client access license could not be upgraded or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="d3896-154"><span id="exDiscReasonLicenseNoRemoteConnections"></span><span id="exdiscreasonlicensenoremoteconnections"></span><span id="EXDISCREASONLICENSENOREMOTECONNECTIONS"></span>**exDiscReasonLicenseNoRemoteConnections**</span><span class="sxs-lookup"><span data-stu-id="d3896-154"><span id="exDiscReasonLicenseNoRemoteConnections"></span><span id="exdiscreasonlicensenoremoteconnections"></span><span id="EXDISCREASONLICENSENOREMOTECONNECTIONS"></span>**exDiscReasonLicenseNoRemoteConnections**</span></span>
</dt> <dd>

<span data-ttu-id="d3896-155">O computador remoto não está licenciado para aceitar conexões remotas.</span><span class="sxs-lookup"><span data-stu-id="d3896-155">The remote computer is not licensed to accept remote connections.</span></span>

</dd> <dt>

<span data-ttu-id="d3896-156"><span id="exDiscReasonLicenseCreatingLicStoreAccDenied"></span><span id="exdiscreasonlicensecreatinglicstoreaccdenied"></span><span id="EXDISCREASONLICENSECREATINGLICSTOREACCDENIED"></span>**exDiscReasonLicenseCreatingLicStoreAccDenied**</span><span class="sxs-lookup"><span data-stu-id="d3896-156"><span id="exDiscReasonLicenseCreatingLicStoreAccDenied"></span><span id="exdiscreasonlicensecreatinglicstoreaccdenied"></span><span id="EXDISCREASONLICENSECREATINGLICSTOREACCDENIED"></span>**exDiscReasonLicenseCreatingLicStoreAccDenied**</span></span>
</dt> <dd>

<span data-ttu-id="d3896-157">Um erro de acesso negado foi recebido ao criar uma chave do registro para o repositório de licenças.</span><span class="sxs-lookup"><span data-stu-id="d3896-157">An access denied error was received while creating a registry key for the license store.</span></span>

</dd> <dt>

<span data-ttu-id="d3896-158"><span id="exDiscReasonRdpEncInvalidCredentials"></span><span id="exdiscreasonrdpencinvalidcredentials"></span><span id="EXDISCREASONRDPENCINVALIDCREDENTIALS"></span>**exDiscReasonRdpEncInvalidCredentials**</span><span class="sxs-lookup"><span data-stu-id="d3896-158"><span id="exDiscReasonRdpEncInvalidCredentials"></span><span id="exdiscreasonrdpencinvalidcredentials"></span><span id="EXDISCREASONRDPENCINVALIDCREDENTIALS"></span>**exDiscReasonRdpEncInvalidCredentials**</span></span>
</dt> <dd>

<span data-ttu-id="d3896-159">Foram encontradas credenciais inválidas.</span><span class="sxs-lookup"><span data-stu-id="d3896-159">Invalid credentials were encountered.</span></span>

</dd> <dt>

<span data-ttu-id="d3896-160"><span id="exDiscReasonProtocolRangeStart"></span><span id="exdiscreasonprotocolrangestart"></span><span id="EXDISCREASONPROTOCOLRANGESTART"></span>**exDiscReasonProtocolRangeStart**</span><span class="sxs-lookup"><span data-stu-id="d3896-160"><span id="exDiscReasonProtocolRangeStart"></span><span id="exdiscreasonprotocolrangestart"></span><span id="EXDISCREASONPROTOCOLRANGESTART"></span>**exDiscReasonProtocolRangeStart**</span></span>
</dt> <dd>

<span data-ttu-id="d3896-161">Começando o intervalo de erros de protocolo interno.</span><span class="sxs-lookup"><span data-stu-id="d3896-161">Beginning the range of internal protocol errors.</span></span> <span data-ttu-id="d3896-162">Verifique o log de eventos do servidor para obter detalhes adicionais.</span><span class="sxs-lookup"><span data-stu-id="d3896-162">Check the server event log for additional details.</span></span>

</dd> <dt>

<span data-ttu-id="d3896-163"><span id="exDiscReasonProtocolRangeEnd"></span><span id="exdiscreasonprotocolrangeend"></span><span id="EXDISCREASONPROTOCOLRANGEEND"></span>**exDiscReasonProtocolRangeEnd**</span><span class="sxs-lookup"><span data-stu-id="d3896-163"><span id="exDiscReasonProtocolRangeEnd"></span><span id="exdiscreasonprotocolrangeend"></span><span id="EXDISCREASONPROTOCOLRANGEEND"></span>**exDiscReasonProtocolRangeEnd**</span></span>
</dt> <dd>

<span data-ttu-id="d3896-164">Encerrando o intervalo de erros de protocolo interno.</span><span class="sxs-lookup"><span data-stu-id="d3896-164">Ending the range of internal protocol errors.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d3896-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3896-165">Requirements</span></span>



| <span data-ttu-id="d3896-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3896-166">Requirement</span></span> | <span data-ttu-id="d3896-167">Valor</span><span class="sxs-lookup"><span data-stu-id="d3896-167">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d3896-168">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d3896-168">Minimum supported client</span></span><br/> | <span data-ttu-id="d3896-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d3896-169">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="d3896-170">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d3896-170">Minimum supported server</span></span><br/> | <span data-ttu-id="d3896-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d3896-171">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="d3896-172">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d3896-172">Type library</span></span><br/>             | <dl> <span data-ttu-id="d3896-173"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3896-173"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3896-174">Confira também</span><span class="sxs-lookup"><span data-stu-id="d3896-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3896-175">**ExtendedDisconnectReason**</span><span class="sxs-lookup"><span data-stu-id="d3896-175">**ExtendedDisconnectReason**</span></span>](imsrdpclient-extendeddisconnectreason.md)
</dt> </dl>

 

 





