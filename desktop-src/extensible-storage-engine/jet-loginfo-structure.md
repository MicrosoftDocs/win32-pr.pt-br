---
description: 'Saiba mais sobre: estrutura de JET_LOGINFO'
title: Estrutura de JET_LOGINFO
TOCTitle: JET_LOGINFO Structure
ms:assetid: b34b3f24-5d19-4e11-a657-a0e59204d628
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294063(v=EXCHG.10)
ms:contentKeyID: 32765678
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b7e643d775d1fb8e0c19286bfb7a50d887644e99
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "105811487"
---
# <a name="jet_loginfo-structure"></a><span data-ttu-id="a77b5-103">Estrutura de JET_LOGINFO</span><span class="sxs-lookup"><span data-stu-id="a77b5-103">JET_LOGINFO Structure</span></span>


<span data-ttu-id="a77b5-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a77b5-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_loginfo-structure"></a><span data-ttu-id="a77b5-105">Estrutura de JET_LOGINFO</span><span class="sxs-lookup"><span data-stu-id="a77b5-105">JET_LOGINFO Structure</span></span>

<span data-ttu-id="a77b5-106">A estrutura de **JET_LOGINFO** retorna informações estruturadas sobre o conjunto de arquivos de log de transações que devem ser parte de um conjunto de arquivos de backup.</span><span class="sxs-lookup"><span data-stu-id="a77b5-106">The **JET_LOGINFO** structure returns structured information about the set of transaction log files that should be a part of a backup file set.</span></span> <span data-ttu-id="a77b5-107">A estrutura de **JET_LOGINFO** é o conjunto mínimo de informações necessárias para representar um intervalo de logs que é recuperado com [JetGetLogInfoInstance2](./jetgetloginfoinstance2-function.md) ou especificado para uma recuperação complexa com [JetExternalRestore2](./jetexternalrestore2-function.md).</span><span class="sxs-lookup"><span data-stu-id="a77b5-107">The **JET_LOGINFO** structure is the minimal set of information needed to represent a range of logs that is retrieved with [JetGetLogInfoInstance2](./jetgetloginfoinstance2-function.md) or specified for a hard recovery with [JetExternalRestore2](./jetexternalrestore2-function.md).</span></span>

```cpp
typedef struct {
  unsigned long cbSize;
  unsigned long ulGenLow;
  unsigned long ulGenHigh;
  tchar szBaseName[JET_BASE_NAME_LENGTH + 1];
} JET_LOGINFO;
```

### <a name="members"></a><span data-ttu-id="a77b5-108">Membros</span><span class="sxs-lookup"><span data-stu-id="a77b5-108">Members</span></span>

<span data-ttu-id="a77b5-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="a77b5-109">**cbSize**</span></span>

<span data-ttu-id="a77b5-110">O tamanho da estrutura, em bytes.</span><span class="sxs-lookup"><span data-stu-id="a77b5-110">The size of the structure, in bytes.</span></span>

<span data-ttu-id="a77b5-111">Esse membro permite a expansão futura dessa estrutura, ao mesmo tempo em que habilita a compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="a77b5-111">This member enables future expansion of this structure while enabling backwards compatibility.</span></span> <span data-ttu-id="a77b5-112">Ele deve sempre ser definido como sizeof (JET_LOGINFO).</span><span class="sxs-lookup"><span data-stu-id="a77b5-112">It should always be set to sizeof( JET_LOGINFO ).</span></span>

<span data-ttu-id="a77b5-113">**ulGenLow**</span><span class="sxs-lookup"><span data-stu-id="a77b5-113">**ulGenLow**</span></span>

<span data-ttu-id="a77b5-114">O número do arquivo de log mais baixo (ou mais antigo) que é restaurado.</span><span class="sxs-lookup"><span data-stu-id="a77b5-114">The lowest (or oldest) log file number that is restored.</span></span> <span data-ttu-id="a77b5-115">A fidelidade total de um longo não assinado deve ser preservada, mas nas versões atuais do mecanismo esse número é um número hexadecimal no intervalo de 0x00000 a 0xFFFFF.</span><span class="sxs-lookup"><span data-stu-id="a77b5-115">The full fidelity of an unsigned long should be preserved, but in current versions of the engine this number is a hexadecimal number in the range from 0x00000 to 0xFFFFF.</span></span> <span data-ttu-id="a77b5-116">Isso pode ser alterado em versões futuras.</span><span class="sxs-lookup"><span data-stu-id="a77b5-116">This might change in future versions.</span></span>

<span data-ttu-id="a77b5-117">**ulGenHigh**</span><span class="sxs-lookup"><span data-stu-id="a77b5-117">**ulGenHigh**</span></span>

<span data-ttu-id="a77b5-118">O número de arquivo de log mais alto (ou mais recente) que é restaurado.</span><span class="sxs-lookup"><span data-stu-id="a77b5-118">The highest (or most recent) log file number that is restored.</span></span> <span data-ttu-id="a77b5-119">A fidelidade total de um longo não assinado deve ser preservada, mas nas versões atuais do mecanismo esse número é um número hexadecimal no intervalo de 0x00000 a 0xFFFFF.</span><span class="sxs-lookup"><span data-stu-id="a77b5-119">The full fidelity of a unsigned long should be preserved, but in current versions of the engine this number is a hexadecimal number in the range from 0x00000 to 0xFFFFF.</span></span> <span data-ttu-id="a77b5-120">Isso pode ser alterado em versões futuras.</span><span class="sxs-lookup"><span data-stu-id="a77b5-120">This might change in future versions.</span></span>

<span data-ttu-id="a77b5-121">**szBaseName**</span><span class="sxs-lookup"><span data-stu-id="a77b5-121">**szBaseName**</span></span>

<span data-ttu-id="a77b5-122">O prefixo usado para nomear os arquivos de log de transações.</span><span class="sxs-lookup"><span data-stu-id="a77b5-122">The prefix used to name the transaction log files.</span></span>

<span data-ttu-id="a77b5-123">O valor retornado nesse membro é sempre igual à configuração de [JET_paramBaseName](./transaction-log-parameters.md) para a instância que gerou essas informações.</span><span class="sxs-lookup"><span data-stu-id="a77b5-123">The value that is returned in this member is always equal to the setting for [JET_paramBaseName](./transaction-log-parameters.md) for the instance that generated this information.</span></span>

### <a name="remarks"></a><span data-ttu-id="a77b5-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="a77b5-124">Remarks</span></span>

<span data-ttu-id="a77b5-125">Os arquivos de log de transações são nomeados de acordo com o nome base da instância e o número de geração do arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="a77b5-125">Transaction log files are named according to the instance base name and the generation number of the log file.</span></span> <span data-ttu-id="a77b5-126">O nome é do formato BBBXXXXX. Façam.</span><span class="sxs-lookup"><span data-stu-id="a77b5-126">The name is of the format BBBXXXXX.LOG.</span></span> <span data-ttu-id="a77b5-127">BBB corresponde ao nome de base para o arquivo de log e tem sempre três caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="a77b5-127">BBB corresponds to the base name for the log file and is always three characters in length.</span></span> <span data-ttu-id="a77b5-128">XXXXX corresponde ao número de geração do arquivo de log em zero hexadecimal preenchido e tem sempre cinco caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="a77b5-128">XXXXX corresponds to the generation number of the log file in zero padded hexadecimal and is always five characters in length.</span></span> <span data-ttu-id="a77b5-129">LOG é a extensão de arquivo que é sempre fornecida para os arquivos de log de transações pelo mecanismo.</span><span class="sxs-lookup"><span data-stu-id="a77b5-129">LOG is the file extension that is always given to transaction log files by the engine.</span></span>

<span data-ttu-id="a77b5-130">O uso dessas informações estruturadas não é recomendado porque faz com que o aplicativo tenha conhecimento profundo desse esquema de nomenclatura para arquivos de log de transações.</span><span class="sxs-lookup"><span data-stu-id="a77b5-130">Use of this structured information is discouraged because it causes the application to have intimate knowledge of this naming scheme for transaction log files.</span></span> <span data-ttu-id="a77b5-131">Se o esquema de nomenclatura mudar no futuro, tal aplicativo deixará de funcionar corretamente.</span><span class="sxs-lookup"><span data-stu-id="a77b5-131">If the naming scheme ever changes in the future then such an application will no longer function properly.</span></span> <span data-ttu-id="a77b5-132">É concebível que o formato de log seja alterado para incorporar 8 dígitos hexadecimais no futuro.</span><span class="sxs-lookup"><span data-stu-id="a77b5-132">It is conceivable that the log format will change to incorporate 8 hex digits in the future.</span></span> <span data-ttu-id="a77b5-133">Os aplicativos devem usar a lista explícita de nomes de arquivos retornados por [JetGetLogInfo](./jetgetloginfo-function.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="a77b5-133">Applications should use the explicit list of file names returned by [JetGetLogInfo](./jetgetloginfo-function.md) instead.</span></span>

### <a name="requirements"></a><span data-ttu-id="a77b5-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a77b5-134">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a77b5-135"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="a77b5-135"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a77b5-136">Requer o Windows Vista ou o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a77b5-136">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a77b5-137"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="a77b5-137"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a77b5-138">Requer o Windows Server 2008 ou o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a77b5-138">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a77b5-139"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="a77b5-139"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a77b5-140">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="a77b5-140">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a77b5-141"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="a77b5-141"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="a77b5-142">Implementado como <strong>JET_LOGINFO_W</strong> (Unicode) e <strong>JET_LOGINFO_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="a77b5-142">Implemented as <strong>JET_LOGINFO_W</strong> (Unicode) and <strong>JET_LOGINFO_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="a77b5-143">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="a77b5-143">See Also</span></span>

[<span data-ttu-id="a77b5-144">JetExternalRestore2</span><span class="sxs-lookup"><span data-stu-id="a77b5-144">JetExternalRestore2</span></span>](./jetexternalrestore2-function.md)  
[<span data-ttu-id="a77b5-145">JetGetLogInfo</span><span class="sxs-lookup"><span data-stu-id="a77b5-145">JetGetLogInfo</span></span>](./jetgetloginfo-function.md)  
[<span data-ttu-id="a77b5-146">JetGetLogInfoInstance2</span><span class="sxs-lookup"><span data-stu-id="a77b5-146">JetGetLogInfoInstance2</span></span>](./jetgetloginfoinstance2-function.md)  
[<span data-ttu-id="a77b5-147">Parâmetros do sistema</span><span class="sxs-lookup"><span data-stu-id="a77b5-147">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
