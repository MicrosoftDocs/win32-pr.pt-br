---
title: Outras constantes de sessão (WSManDisp. h)
description: Especifique a codificação, a criptografia e a porta do nome da entidade de serviço.
ms.assetid: a921b7bc-1f40-427c-971f-c0bc9c9f6887
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- WSManFlagUTF8
- WSManFlagNoEncryption
- WSManFlagEnableSPNServerPort
- WSManFlagUTF16
api_location:
- WSManDisp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 236e69d80db2ad30b8cc2934b6b2016d7eecbed6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086206"
---
# <a name="other-session-constants"></a><span data-ttu-id="30725-103">Outras constantes de sessão</span><span class="sxs-lookup"><span data-stu-id="30725-103">Other Session Constants</span></span>

<span data-ttu-id="30725-104">Constantes, listadas na lista a seguir, na enumeração **\_ \_ WSManSessionFlags** que especificam a codificação, a criptografia e a porta do nome da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="30725-104">Constants, listed in the following list, in the **\_\_WSManSessionFlags** enumeration that specify encoding, encryption, and service principal name port.</span></span>

<dl> <dt>

<span data-ttu-id="30725-105"><span id="WSManFlagUTF8"></span><span id="wsmanflagutf8"></span><span id="WSMANFLAGUTF8"></span>**WSManFlagUTF8**</span><span class="sxs-lookup"><span data-stu-id="30725-105"><span id="WSManFlagUTF8"></span><span id="wsmanflagutf8"></span><span id="WSMANFLAGUTF8"></span>**WSManFlagUTF8**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30725-106">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="30725-106">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="30725-107">Envia a solicitação em UTF8 em vez de UTF16.</span><span class="sxs-lookup"><span data-stu-id="30725-107">Sends the request in UTF8 rather than UTF16.</span></span>

<span data-ttu-id="30725-108">O método de script associado é [**WSMan. SessionFlagUTF8**](wsman-sessionflagutf8.md) e o método C++ é [**IWSManEx. SessionFlagUTF8**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagutf8).</span><span class="sxs-lookup"><span data-stu-id="30725-108">The associated scripting method is [**WSMan.SessionFlagUTF8**](wsman-sessionflagutf8.md) and the C++ method is [**IWSManEx.SessionFlagUTF8**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagutf8).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="30725-109"><span id="WSManFlagNoEncryption"></span><span id="wsmanflagnoencryption"></span><span id="WSMANFLAGNOENCRYPTION"></span>**WSManFlagNoEncryption**</span><span class="sxs-lookup"><span data-stu-id="30725-109"><span id="WSManFlagNoEncryption"></span><span id="wsmanflagnoencryption"></span><span id="WSMANFLAGNOENCRYPTION"></span>**WSManFlagNoEncryption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30725-110">1048576 (0x100000)</span><span class="sxs-lookup"><span data-stu-id="30725-110">1048576 (0x100000)</span></span>
</dt> <dt>



<span data-ttu-id="30725-111">Não criptografe as mensagens enviadas pela rede.</span><span class="sxs-lookup"><span data-stu-id="30725-111">Do not encrypt the messages sent over the network.</span></span> <span data-ttu-id="30725-112">Essa configuração só será permitida se o [*ouvinte*](windows-remote-management-glossary.md) estiver configurado para que **AllowUnencrypted** seja definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="30725-112">This setting is allowed only if the [*listener*](windows-remote-management-glossary.md) is configured so that **AllowUnencrypted** is set to **True**.</span></span>

<span data-ttu-id="30725-113">O método de script associado é [**WSMan. SessionFlagNoEncryption**](wsman-sessionflagnoencryption.md) e o método C++ é [**IWSManEx. SessionFlagNoEncryption**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagnoencryption).</span><span class="sxs-lookup"><span data-stu-id="30725-113">The associated scripting method is [**WSMan.SessionFlagNoEncryption**](wsman-sessionflagnoencryption.md) and the C++ method is [**IWSManEx.SessionFlagNoEncryption**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagnoencryption).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="30725-114"><span id="WSManFlagEnableSPNServerPort"></span><span id="wsmanflagenablespnserverport"></span><span id="WSMANFLAGENABLESPNSERVERPORT"></span>**WSManFlagEnableSPNServerPort**</span><span class="sxs-lookup"><span data-stu-id="30725-114"><span id="WSManFlagEnableSPNServerPort"></span><span id="wsmanflagenablespnserverport"></span><span id="WSMANFLAGENABLESPNSERVERPORT"></span>**WSManFlagEnableSPNServerPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30725-115">4194304 (0x400000)</span><span class="sxs-lookup"><span data-stu-id="30725-115">4194304 (0x400000)</span></span>
</dt> <dt>



<span data-ttu-id="30725-116">Especifique a porta do SPN (nome da entidade de serviço) ao se conectar diretamente ao hardware do BMC remoto, também conhecido como uma conexão [*fora de banda*](windows-remote-management-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="30725-116">Specify the Service Principal Name (SPN) port when connecting directly to remote BMC hardware, also known as an [*out-of-band*](windows-remote-management-glossary.md) connection.</span></span> <span data-ttu-id="30725-117">Como o computador do servidor WinRM e o hardware BMC podem compartilhar o mesmo endereço IP, esse sinalizador indica que o número da porta SPN deve ser usado para determinar se a conexão é para o serviço ou diretamente para o BMC.</span><span class="sxs-lookup"><span data-stu-id="30725-117">Because both the WinRM server computer and the BMC hardware can share the same IP address, this flag indicates that the SPN port number must be used to determine whether the connection is to the service or directly to the BMC.</span></span> <span data-ttu-id="30725-118">Para obter mais informações, consulte [formatos de nome para SPNs exclusivos](/windows/desktop/AD/name-formats-for-unique-spns).</span><span class="sxs-lookup"><span data-stu-id="30725-118">For more information, see [Name Formats for Unique SPNs](/windows/desktop/AD/name-formats-for-unique-spns).</span></span>

<span data-ttu-id="30725-119">O método de script associado é [**WSMan. SessionFlagEnableSPNServerPort**](wsman-sessionflagenablespnserverport.md) e o método C++ é [**IWSManEx. SessionFlagEnableSPNServerPort**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagenablespnserverport).</span><span class="sxs-lookup"><span data-stu-id="30725-119">The associated scripting method is [**WSMan.SessionFlagEnableSPNServerPort**](wsman-sessionflagenablespnserverport.md) and the C++ method is [**IWSManEx.SessionFlagEnableSPNServerPort**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagenablespnserverport).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="30725-120"><span id="WSManFlagUTF16"></span><span id="wsmanflagutf16"></span><span id="WSMANFLAGUTF16"></span>**WSManFlagUTF16**</span><span class="sxs-lookup"><span data-stu-id="30725-120"><span id="WSManFlagUTF16"></span><span id="wsmanflagutf16"></span><span id="WSMANFLAGUTF16"></span>**WSManFlagUTF16**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30725-121">0x800000</span><span class="sxs-lookup"><span data-stu-id="30725-121">0x800000</span></span>
</dt> <dt>



<span data-ttu-id="30725-122">Envia a solicitação em UTF16.</span><span class="sxs-lookup"><span data-stu-id="30725-122">Sends the request in UTF16.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="30725-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30725-123">Requirements</span></span>



| <span data-ttu-id="30725-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="30725-124">Requirement</span></span> | <span data-ttu-id="30725-125">Valor</span><span class="sxs-lookup"><span data-stu-id="30725-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="30725-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="30725-126">Minimum supported client</span></span><br/> | <span data-ttu-id="30725-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="30725-127">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="30725-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="30725-128">Minimum supported server</span></span><br/> | <span data-ttu-id="30725-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="30725-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="30725-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="30725-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="30725-131"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="30725-131"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="30725-132">INSERI</span><span class="sxs-lookup"><span data-stu-id="30725-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="30725-133"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="30725-133"><dt>WSManDisp.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30725-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="30725-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30725-135">Constantes de sessão</span><span class="sxs-lookup"><span data-stu-id="30725-135">Session Constants</span></span>](session-constants.md)
</dt> </dl>

 

