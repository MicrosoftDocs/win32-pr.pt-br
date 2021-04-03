---
title: Fragmento
description: Use o pacote de fragmento para enviar um fragmento do arquivo de upload para o servidor.
ms.assetid: d6df7e47-a240-4be2-a9c4-24a13e622861
keywords:
- BITS de fragmento
topic_type:
- apiref
api_name:
- Fragment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f5103e90ec84a20ff4c04d9036a744919d9b1fd
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104084364"
---
# <a name="fragment"></a><span data-ttu-id="2e5df-104">Fragmento</span><span class="sxs-lookup"><span data-stu-id="2e5df-104">Fragment</span></span>

<span data-ttu-id="2e5df-105">Use o pacote de **fragmento** para enviar um fragmento do arquivo de upload para o servidor.</span><span class="sxs-lookup"><span data-stu-id="2e5df-105">Use the **Fragment** packet to send a fragment of the upload file to the server.</span></span>

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Fragment
BITS-Session-Id: {guid}
Content-Name: filename
Content-Length: length
Content-Range: Bytes range/total-length
Content-Encoding: encoding
```

## <a name="headers"></a><span data-ttu-id="2e5df-106">Cabeçalhos</span><span class="sxs-lookup"><span data-stu-id="2e5df-106">Headers</span></span>

<dl> <dt>

<span data-ttu-id="2e5df-107"><span id="BITS_POST"></span><span id="bits_post"></span>\_postagem de bits</span><span class="sxs-lookup"><span data-stu-id="2e5df-107"><span id="BITS_POST"></span><span id="bits_post"></span>BITS\_POST</span></span>
</dt> <dd>

<span data-ttu-id="2e5df-108">Verbo específico do BITS que identifica esse pacote para o servidor BITS.</span><span class="sxs-lookup"><span data-stu-id="2e5df-108">BITS-specific verb that identifies this packet to the BITS server.</span></span>

<span data-ttu-id="2e5df-109">Substitua a URL remota pelo URI absoluto ou relativo.</span><span class="sxs-lookup"><span data-stu-id="2e5df-109">Replace remote-URL with the absolute or relative URI.</span></span> <span data-ttu-id="2e5df-110">Normalmente, substitua a URL remota pelo nome do arquivo remoto do trabalho.</span><span class="sxs-lookup"><span data-stu-id="2e5df-110">Typically, replace remote-URL with the remote file name of the job.</span></span> <span data-ttu-id="2e5df-111">Para obter considerações sobre balanceamento de carga de rede, consulte o cabeçalho BITS-host-ID no pacote de [**criação de sessão**](create-session.md) .</span><span class="sxs-lookup"><span data-stu-id="2e5df-111">For network load balancing considerations, see the BITS-Host-Id header in the [**Create-Session**](create-session.md) packet.</span></span>

</dd> <dt>

<span data-ttu-id="2e5df-112"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-tipo de pacote</span><span class="sxs-lookup"><span data-stu-id="2e5df-112"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="2e5df-113">Identifica esse pacote de solicitação como um pacote de fragmento.</span><span class="sxs-lookup"><span data-stu-id="2e5df-113">Identifies this request packet as a Fragment packet.</span></span>

</dd> <dt>

<span data-ttu-id="2e5df-114"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-ID da sessão</span><span class="sxs-lookup"><span data-stu-id="2e5df-114"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-Id</span></span>
</dt> <dd>

<span data-ttu-id="2e5df-115">GUID de cadeia de caracteres que identifica a sessão para o servidor.</span><span class="sxs-lookup"><span data-stu-id="2e5df-115">String GUID that identifies the session to the server.</span></span> <span data-ttu-id="2e5df-116">Substitua {GUID} pelo identificador de sessão que o servidor retorna no pacote [**ACK para a resposta de Create-Session**](ack-for-create-session.md) .</span><span class="sxs-lookup"><span data-stu-id="2e5df-116">Replace {guid} with the session identifier that the server returns in the [**Ack for Create-Session**](ack-for-create-session.md) response packet.</span></span>

</dd> <dt>

<span data-ttu-id="2e5df-117"><span id="Content-Name"></span><span id="content-name"></span><span id="CONTENT-NAME"></span>Nome-do-conteúdo</span><span class="sxs-lookup"><span data-stu-id="2e5df-117"><span id="Content-Name"></span><span id="content-name"></span><span id="CONTENT-NAME"></span>Content-Name</span></span>
</dt> <dd>

<span data-ttu-id="2e5df-118">Especifique este cabeçalho somente com o fragmento inicial.</span><span class="sxs-lookup"><span data-stu-id="2e5df-118">Specify this header only with the initial fragment.</span></span> <span data-ttu-id="2e5df-119">Substitua filename pelo nome do nome do arquivo local do trabalho.</span><span class="sxs-lookup"><span data-stu-id="2e5df-119">Replace filename with the name of the local file name from the job.</span></span> <span data-ttu-id="2e5df-120">O nome não inclui o caminho.</span><span class="sxs-lookup"><span data-stu-id="2e5df-120">The name does not include the path.</span></span>

</dd> <dt>

<span data-ttu-id="2e5df-121"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Comprimento do conteúdo</span><span class="sxs-lookup"><span data-stu-id="2e5df-121"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Content-Length</span></span>
</dt> <dd>

<span data-ttu-id="2e5df-122">Substitua o comprimento pelo número de bytes enviados no corpo do fragmento.</span><span class="sxs-lookup"><span data-stu-id="2e5df-122">Replace length with the number of bytes sent in the fragment body.</span></span>

</dd> <dt>

<span data-ttu-id="2e5df-123"><span id="Content-Range"></span><span id="content-range"></span><span id="CONTENT-RANGE"></span>Intervalo de conteúdo</span><span class="sxs-lookup"><span data-stu-id="2e5df-123"><span id="Content-Range"></span><span id="content-range"></span><span id="CONTENT-RANGE"></span>Content-Range</span></span>
</dt> <dd>

<span data-ttu-id="2e5df-124">Informa ao servidor onde aplicar o intervalo no arquivo de destino.</span><span class="sxs-lookup"><span data-stu-id="2e5df-124">Tells the server where to apply the range in the destination file.</span></span> <span data-ttu-id="2e5df-125">Substitua intervalo pelos deslocamentos inicial e final do intervalo no arquivo de destino.</span><span class="sxs-lookup"><span data-stu-id="2e5df-125">Replace range with the start and end offsets of the range in the destination file.</span></span> <span data-ttu-id="2e5df-126">Os deslocamentos são baseados em zero.</span><span class="sxs-lookup"><span data-stu-id="2e5df-126">The offsets are zero-based.</span></span> <span data-ttu-id="2e5df-127">Se o intervalo especificado sobrepor um intervalo existente, o BITS gravará apenas a parte não sobreposta do intervalo; O BITS não substitui o conteúdo existente.</span><span class="sxs-lookup"><span data-stu-id="2e5df-127">If the given range overlaps an existing range, BITS writes only the non-overlapping portion of the range; BITS does not overwrite existing content.</span></span> <span data-ttu-id="2e5df-128">Por exemplo, se o primeiro pacote contiver o intervalo de 0 a 100 e o segundo pacote contiver o intervalo de 50 a 150, o BITS gravará somente os bytes de 101 a 150 do segundo pacote.</span><span class="sxs-lookup"><span data-stu-id="2e5df-128">For example, if the first packet contained the range 0 through 100 and the second packet contained the range 50 through 150, BITS writes only bytes 101 through 150 from the second packet.</span></span> <span data-ttu-id="2e5df-129">Substitua total-Length pelo número total de bytes no arquivo.</span><span class="sxs-lookup"><span data-stu-id="2e5df-129">Replace total-length with the total number of bytes in the file.</span></span>

</dd> <dt>

<span data-ttu-id="2e5df-130"><span id="Content-Encoding"></span><span id="content-encoding"></span><span id="CONTENT-ENCODING"></span>Codificação de conteúdo</span><span class="sxs-lookup"><span data-stu-id="2e5df-130"><span id="Content-Encoding"></span><span id="content-encoding"></span><span id="CONTENT-ENCODING"></span>Content-Encoding</span></span>
</dt> <dd>

<span data-ttu-id="2e5df-131">Substitua Encoding pelo tipo de codificação que o cliente usa no fragmento.</span><span class="sxs-lookup"><span data-stu-id="2e5df-131">Replace encoding with the type of encoding the client uses on the fragment.</span></span> <span data-ttu-id="2e5df-132">O cliente deve usar a codificação que o servidor identifica no cabeçalho Accept-Encoding do ACK para o pacote de resposta de [**Create-Session**](ack-for-create-session.md) .</span><span class="sxs-lookup"><span data-stu-id="2e5df-132">The client must use the encoding that the server identifies in the Accept-Encoding header of the [**Ack for Create-Session**](ack-for-create-session.md) response packet.</span></span> <span data-ttu-id="2e5df-133">O servidor usa o tipo de codificação para decodificar o fragmento.</span><span class="sxs-lookup"><span data-stu-id="2e5df-133">The server uses the encoding type to decode the fragment.</span></span> <span data-ttu-id="2e5df-134">Todos os fragmentos devem especificar a mesma codificação.</span><span class="sxs-lookup"><span data-stu-id="2e5df-134">All fragments must specify the same encoding.</span></span>

<span data-ttu-id="2e5df-135">Não envie esse cabeçalho se o tipo de codificação for Identity.</span><span class="sxs-lookup"><span data-stu-id="2e5df-135">Do not send this header if the encoding type is Identity.</span></span> <span data-ttu-id="2e5df-136">O servidor BITS dá suporte apenas à codificação de identidade.</span><span class="sxs-lookup"><span data-stu-id="2e5df-136">The BITS server supports only Identity encoding.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2e5df-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="2e5df-137">Remarks</span></span>

<span data-ttu-id="2e5df-138">O fragmento é um intervalo de bytes enviados no corpo do pacote.</span><span class="sxs-lookup"><span data-stu-id="2e5df-138">The fragment is a range of bytes sent in the body of the packet.</span></span> <span data-ttu-id="2e5df-139">O cliente envia os fragmentos em ordem sequencial começando com deslocamento zero; o servidor não mantém o controle de intervalos não contíguos.</span><span class="sxs-lookup"><span data-stu-id="2e5df-139">The client sends the fragments in sequential order starting with offset zero; the server does not keep track of non-contiguous ranges.</span></span> <span data-ttu-id="2e5df-140">Se o cliente enviar intervalos não contíguos, o servidor retornará um código de retorno HTTP 416 (intervalo insatisfatório) no [**ACK para a resposta do fragmento**](ack-for-fragment.md) .</span><span class="sxs-lookup"><span data-stu-id="2e5df-140">If the client sends non-contiguous ranges, the server returns an HTTP 416 (range-not-satisfiable) return code in the [**Ack for Fragment**](ack-for-fragment.md) response.</span></span>

<span data-ttu-id="2e5df-141">Os cabeçalhos content-*xxxx* são cabeçalhos HTTP 1,1 padrão.</span><span class="sxs-lookup"><span data-stu-id="2e5df-141">The Content-*xxxx* headers are standard HTTP 1.1 headers.</span></span> <span data-ttu-id="2e5df-142">Para obter mais detalhes sobre os cabeçalhos content-*xxxx* , consulte a especificação [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt) .</span><span class="sxs-lookup"><span data-stu-id="2e5df-142">For more details on the Content-*xxxx* headers, see the [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt) specification.</span></span>

## <a name="see-also"></a><span data-ttu-id="2e5df-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="2e5df-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e5df-144">**Confirmação para fragmento**</span><span class="sxs-lookup"><span data-stu-id="2e5df-144">**Ack for Fragment**</span></span>](ack-for-fragment.md)
</dt> <dt>

[<span data-ttu-id="2e5df-145">**Fechar sessão**</span><span class="sxs-lookup"><span data-stu-id="2e5df-145">**Close-Session**</span></span>](close-session.md)
</dt> <dt>

[<span data-ttu-id="2e5df-146">**Criar sessão**</span><span class="sxs-lookup"><span data-stu-id="2e5df-146">**Create-Session**</span></span>](create-session.md)
</dt> </dl>

 

 




