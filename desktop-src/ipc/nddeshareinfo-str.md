---
description: Contém atributos de compartilhamento DDE mantidos pelo Gerenciador de banco de dados de compartilhamento NetDDE (DSDM).
ms.assetid: f4101553-06ef-4f83-87c7-5b6fdf0467e5
title: Estrutura NDDESHAREINFO (Nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDDESHAREINFO
api_type:
- HeaderDef
api_location:
- Nddeapi.h
ms.openlocfilehash: 975382272a4e2c7cc56b0ddf593905b4d745a48b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812187"
---
# <a name="nddeshareinfo-structure"></a><span data-ttu-id="0e174-103">Estrutura NDDESHAREINFO</span><span class="sxs-lookup"><span data-stu-id="0e174-103">NDDESHAREINFO structure</span></span>

<span data-ttu-id="0e174-104">\[Não há mais suporte para DDE de rede.</span><span class="sxs-lookup"><span data-stu-id="0e174-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="0e174-105">Nddeapi.dll está presente no Windows Vista, mas todas as chamadas de função retornam NDDE \_ não \_ implementado.\]</span><span class="sxs-lookup"><span data-stu-id="0e174-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="0e174-106">Contém atributos de compartilhamento DDE mantidos pelo Gerenciador de banco de dados de compartilhamento NetDDE (DSDM).</span><span class="sxs-lookup"><span data-stu-id="0e174-106">Contains DDE share attributes maintained by the NetDDE Share Database Manager (DSDM).</span></span> <span data-ttu-id="0e174-107">O descritor de segurança associado a cada compartilhamento DDE não é passado por essa estrutura, mas é acessado por meio de funções específicas.</span><span class="sxs-lookup"><span data-stu-id="0e174-107">The security descriptor associated with each DDE share is not passed through this structure but is accessed through specific functions.</span></span> <span data-ttu-id="0e174-108">A API do NetDDE DSDM aceita essa estrutura para funções Set; para funções Get, o DSDM retorna a estrutura empacotada no buffer fornecido junto com os dados referenciados pelos membros **lpszShareName**, **lpszAppTopicList** e **lpszItemList**.</span><span class="sxs-lookup"><span data-stu-id="0e174-108">The NetDDE DSDM API accepts this structure for set functions; for get functions, the DSDM returns the structure packed into the supplied buffer along with the data referenced by the members **lpszShareName**, **lpszAppTopicList**, and **lpszItemList**.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e174-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0e174-109">Syntax</span></span>


```C++
typedef struct _NDDESHAREINFO {
  LONG   lRevision;
  LPTSTR lpszShareName;
  LONG   lShareType;
  LPTSTR lpszAppTopicList;
  LONG   fSharedFlag;
  LONG   fService;
  LONG   fStartAppFlag;
  LONG   nCmdShow;
  LONG   qModifyId[2];
  LONG   cNumItems;
  LPTSTR lpszItemList;
} NDDESHAREINFO, *PNDDESHAREINFO;
```



## <a name="members"></a><span data-ttu-id="0e174-110">Membros</span><span class="sxs-lookup"><span data-stu-id="0e174-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="0e174-111">**lRevision**</span><span class="sxs-lookup"><span data-stu-id="0e174-111">**lRevision**</span></span>
</dt> <dd>

<span data-ttu-id="0e174-112">O nível de revisão da estrutura **NDDESHAREINFO** .</span><span class="sxs-lookup"><span data-stu-id="0e174-112">The revision level of the **NDDESHAREINFO** structure.</span></span> <span data-ttu-id="0e174-113">Atualmente, o nível de revisão é 1.</span><span class="sxs-lookup"><span data-stu-id="0e174-113">Currently, the revision level is 1.</span></span>

</dd> <dt>

<span data-ttu-id="0e174-114">**lpszShareName**</span><span class="sxs-lookup"><span data-stu-id="0e174-114">**lpszShareName**</span></span>
</dt> <dd>

<span data-ttu-id="0e174-115">O nome do compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="0e174-115">The name of the share.</span></span> <span data-ttu-id="0e174-116">Essa cadeia de caracteres não deve ter mais do que o máximo de \_ NDDESHARENAME caracteres.</span><span class="sxs-lookup"><span data-stu-id="0e174-116">This string must be no more than MAX\_NDDESHARENAME characters long.</span></span>

</dd> <dt>

<span data-ttu-id="0e174-117">**lShareType**</span><span class="sxs-lookup"><span data-stu-id="0e174-117">**lShareType**</span></span>
</dt> <dd>

<span data-ttu-id="0e174-118">Um ou mais tipos de compartilhamento DDE.</span><span class="sxs-lookup"><span data-stu-id="0e174-118">One or more DDE share types.</span></span> <span data-ttu-id="0e174-119">Esse membro pode ser uma combinação dos seguintes tipos de compartilhamento de DDE com suporte.</span><span class="sxs-lookup"><span data-stu-id="0e174-119">This member can be a combination of the following supported DDE share types.</span></span>



| <span data-ttu-id="0e174-120">Tipo de compartilhamento</span><span class="sxs-lookup"><span data-stu-id="0e174-120">Share type</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="0e174-121">Significado</span><span class="sxs-lookup"><span data-stu-id="0e174-121">Meaning</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="SHARE_TYPE_NEW"></span><span id="share_type_new"></span><dl> <span data-ttu-id="0e174-122"><dt>**Compartilhar \_ Digite \_ novo**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="0e174-122"><dt>**SHARE\_TYPE\_NEW**</dt> <dt>0x02</dt></span></span> </dl>          | <span data-ttu-id="0e174-123">O compartilhamento contém um par de aplicativo/tópico OLE.</span><span class="sxs-lookup"><span data-stu-id="0e174-123">The share contains an OLE application/topic pair.</span></span><br/>   |
| <span id="SHARE_TYPE_OLD"></span><span id="share_type_old"></span><dl> <span data-ttu-id="0e174-124"><dt>**Compartilhar \_ Digite \_ antigo**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="0e174-124"><dt>**SHARE\_TYPE\_OLD**</dt> <dt>0x01</dt></span></span> </dl>          | <span data-ttu-id="0e174-125">O compartilhamento contém um par de aplicativo/tópico DDE.</span><span class="sxs-lookup"><span data-stu-id="0e174-125">The share contains a DDE application/topic pair.</span></span><br/>    |
| <span id="SHARE_TYPE_STATIC"></span><span id="share_type_static"></span><dl> <span data-ttu-id="0e174-126"><dt>**Compartilhar \_ Digite \_**</dt> <dt>0x04</dt> estático</span><span class="sxs-lookup"><span data-stu-id="0e174-126"><dt>**SHARE\_TYPE\_STATIC**</dt> <dt>0x04</dt></span></span> </dl> | <span data-ttu-id="0e174-127">O compartilhamento contém um par de aplicativo/tópico estático.</span><span class="sxs-lookup"><span data-stu-id="0e174-127">The share contains a static application/topic pair.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0e174-128">**lpszAppTopicList**</span><span class="sxs-lookup"><span data-stu-id="0e174-128">**lpszAppTopicList**</span></span>
</dt> <dd>

<span data-ttu-id="0e174-129">Um ponteiro para um buffer que contém cadeias de caracteres terminadas em nulo para os pares de aplicativo/tópico estáticos, OLE e DDE.</span><span class="sxs-lookup"><span data-stu-id="0e174-129">A pointer to a buffer containing null-terminated strings for the DDE, OLE, and static application/topic pairs.</span></span> <span data-ttu-id="0e174-130">O buffer deve estar no seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="0e174-130">The buffer should be in the following format:</span></span>

``` syntax
<DDE application name>|<DDE topic name>\0
<OLE application name>|<OLE topic name>\0
<static application name>|<static topic name>\0\0
```

</dd> <dt>

<span data-ttu-id="0e174-131">**fSharedFlag**</span><span class="sxs-lookup"><span data-stu-id="0e174-131">**fSharedFlag**</span></span>
</dt> <dd>

<span data-ttu-id="0e174-132">Se esse membro for **falso**, o compartilhamento DDE não permitirá que os usuários remotos se comuniquem através dele usando o DDE.</span><span class="sxs-lookup"><span data-stu-id="0e174-132">If this member is **FALSE**, the DDE share will not allow remote users to communicate through it by using DDE.</span></span> <span data-ttu-id="0e174-133">No entanto, os usuários locais ainda podem se comunicar por meio do compartilhamento DDE.</span><span class="sxs-lookup"><span data-stu-id="0e174-133">However, local users can still communicate through the DDE share.</span></span> <span data-ttu-id="0e174-134">Os links de cliente local serão sempre inferidos se a DACL associada conceder acesso.</span><span class="sxs-lookup"><span data-stu-id="0e174-134">Local client links are always implied if the associated DACL grants access.</span></span>

</dd> <dt>

<span data-ttu-id="0e174-135">**fService**</span><span class="sxs-lookup"><span data-stu-id="0e174-135">**fService**</span></span>
</dt> <dd>

<span data-ttu-id="0e174-136">Se esse membro estiver definido, o compartilhamento DDE não verificará se o usuário atual o definiu como confiável antes de permitir a comunicação DDE.</span><span class="sxs-lookup"><span data-stu-id="0e174-136">If this member is set, the DDE share will not check whether the current user has set it as trusted before allowing DDE communication.</span></span>

</dd> <dt>

<span data-ttu-id="0e174-137">**fStartAppFlag**</span><span class="sxs-lookup"><span data-stu-id="0e174-137">**fStartAppFlag**</span></span>
</dt> <dd>

<span data-ttu-id="0e174-138">Se esse membro estiver definido e o compartilhamento for confiável para iniciar aplicativos, o NetDDE tentará iniciar o aplicativo especificado por **lpszAppTopicList** se ele não puder iniciar inicialmente uma conversa DDE com o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0e174-138">If this member is set and the share is trusted to start applications, NetDDE will attempt to start the application specified by **lpszAppTopicList** if it cannot initially start a DDE conversation with the application.</span></span>

</dd> <dt>

<span data-ttu-id="0e174-139">**nCmdShow**</span><span class="sxs-lookup"><span data-stu-id="0e174-139">**nCmdShow**</span></span>
</dt> <dd>

<span data-ttu-id="0e174-140">Quando o NetDDE inicia um aplicativo para iniciar uma conversa DDE, esse valor é enviado para o aplicativo por meio do parâmetro *nCmdShow* da função [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) .</span><span class="sxs-lookup"><span data-stu-id="0e174-140">When NetDDE starts an application to initiate a DDE conversation, this value is sent to the application through the *nCmdShow* parameter of the [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) function.</span></span> <span data-ttu-id="0e174-141">Ele define o modo preferencial para a janela do aplicativo a ser mostrada no.</span><span class="sxs-lookup"><span data-stu-id="0e174-141">It defines the preferred mode for the application window to be shown in.</span></span> <span data-ttu-id="0e174-142">Esse parâmetro será significativo somente se **fStartAppFlag** estiver ativo.</span><span class="sxs-lookup"><span data-stu-id="0e174-142">This parameter is significant only if **fStartAppFlag** is active.</span></span> <span data-ttu-id="0e174-143">O usuário conectado em cujo contexto o aplicativo é iniciado também pode substituir essa opção ao promover o compartilhamento para o status confiável.</span><span class="sxs-lookup"><span data-stu-id="0e174-143">The logged on user in whose context the application is started can also override this option when promoting the share to trusted status.</span></span> <span data-ttu-id="0e174-144">O padrão para esse membro é SW \_ PERmaximed.</span><span class="sxs-lookup"><span data-stu-id="0e174-144">The default for this member is SW\_SHOWMAXIMIZED.</span></span>

</dd> <dt>

<span data-ttu-id="0e174-145">**qModifyId**</span><span class="sxs-lookup"><span data-stu-id="0e174-145">**qModifyId**</span></span>
</dt> <dd>

<span data-ttu-id="0e174-146">Um número de série de 8 bytes que indica o número de série de modificação do compartilhamento DDE.</span><span class="sxs-lookup"><span data-stu-id="0e174-146">An 8-byte serial number that indicates the modification serial number of the DDE share.</span></span> <span data-ttu-id="0e174-147">Toda vez que o compartilhamento DDE é modificado por uma chamada [**NDdeShareSetInfo**](nddesharesetinfo.md) ou [**NDdeSetShareSecurity**](nddesetsharesecurity.md) , esses valores são alterados.</span><span class="sxs-lookup"><span data-stu-id="0e174-147">Every time the DDE share is modified by a [**NDdeShareSetInfo**](nddesharesetinfo.md) or [**NDdeSetShareSecurity**](nddesetsharesecurity.md) call, these values are changed.</span></span>

</dd> <dt>

<span data-ttu-id="0e174-148">**cNumItems**</span><span class="sxs-lookup"><span data-stu-id="0e174-148">**cNumItems**</span></span>
</dt> <dd>

<span data-ttu-id="0e174-149">O número de itens listados em **lpszItemList**.</span><span class="sxs-lookup"><span data-stu-id="0e174-149">The number of items listed in **lpszItemList**.</span></span> <span data-ttu-id="0e174-150">Se **cNumItems** for zero, **lpszItemList** estará vazio e as informações de compartilhamento e o descritor de segurança associado serão aplicados a todos os itens atendidos pelo aplicativo associado.</span><span class="sxs-lookup"><span data-stu-id="0e174-150">If **cNumItems** is zero, then **lpszItemList** is empty, and the share information and associated security descriptor apply to all items serviced by the associated application.</span></span>

</dd> <dt>

<span data-ttu-id="0e174-151">**lpszItemList**</span><span class="sxs-lookup"><span data-stu-id="0e174-151">**lpszItemList**</span></span>
</dt> <dd>

<span data-ttu-id="0e174-152">Um ponteiro para um buffer que contém cadeias de caracteres terminadas em nulo que especificam os itens em que o aplicativo cliente em uma transação DDE pode solicitar ou iniciar loops de aviso.</span><span class="sxs-lookup"><span data-stu-id="0e174-152">A pointer to a buffer containing null-terminated strings that specify the items the client application in a DDE transaction can request or start advise loops on.</span></span> <span data-ttu-id="0e174-153">Se nenhum item estiver listado, o compartilhamento de DDE permitirá que todos os itens sejam usados.</span><span class="sxs-lookup"><span data-stu-id="0e174-153">If no items are listed, the DDE share allows any item to be used.</span></span> <span data-ttu-id="0e174-154">O número de itens na lista deve corresponder à contagem de **cNumItems** .</span><span class="sxs-lookup"><span data-stu-id="0e174-154">The number of items in the list must match the **cNumItems** count.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0e174-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e174-155">Requirements</span></span>



| <span data-ttu-id="0e174-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e174-156">Requirement</span></span> | <span data-ttu-id="0e174-157">Valor</span><span class="sxs-lookup"><span data-stu-id="0e174-157">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0e174-158">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0e174-158">Minimum supported client</span></span><br/> | <span data-ttu-id="0e174-159">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0e174-159">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="0e174-160">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0e174-160">Minimum supported server</span></span><br/> | <span data-ttu-id="0e174-161">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0e174-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="0e174-162">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0e174-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e174-163"><dt>Nddeapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e174-163"><dt>Nddeapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e174-164">Confira também</span><span class="sxs-lookup"><span data-stu-id="0e174-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e174-165">Visão geral de troca dinâmica de dados de rede</span><span class="sxs-lookup"><span data-stu-id="0e174-165">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="0e174-166">Estruturas DDE de rede</span><span class="sxs-lookup"><span data-stu-id="0e174-166">Network DDE Structures</span></span>](network-dde-structures.md)
</dt> <dt>

[<span data-ttu-id="0e174-167">**NDdeSetShareSecurity**</span><span class="sxs-lookup"><span data-stu-id="0e174-167">**NDdeSetShareSecurity**</span></span>](nddesetsharesecurity.md)
</dt> <dt>

[<span data-ttu-id="0e174-168">**NDdeShareSetInfo**</span><span class="sxs-lookup"><span data-stu-id="0e174-168">**NDdeShareSetInfo**</span></span>](nddesharesetinfo.md)
</dt> <dt>

[<span data-ttu-id="0e174-169">**WinMain**</span><span class="sxs-lookup"><span data-stu-id="0e174-169">**WinMain**</span></span>](/windows/win32/api/winbase/nf-winbase-winmain)
</dt> </dl>

 

