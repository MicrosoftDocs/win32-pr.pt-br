---
title: O arquivo de proxy da interface
description: O arquivo de proxy de interface (U \_ p. c) é um arquivo c que contém rotinas equivalentes aos dos arquivos stub de cliente e stub de servidor de uma interface de objeto (com).
ms.assetid: f85f7384-a590-4146-9705-2e87f1a0a87a
keywords:
- MIDL e MIDL COM, interfaces, arquivos de proxy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7be52b3561af03df0375212d729f64f41e3cdd7b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916459"
---
# <a name="the-interface-proxy-file"></a><span data-ttu-id="f025a-104">O arquivo de proxy da interface</span><span class="sxs-lookup"><span data-stu-id="f025a-104">The Interface Proxy File</span></span>

<span data-ttu-id="f025a-105">O arquivo de proxy de interface (U \_ p. c) é um arquivo c que contém rotinas equivalentes aos dos arquivos stub de cliente e stub de servidor de uma interface de objeto (com).</span><span class="sxs-lookup"><span data-stu-id="f025a-105">The interface proxy file (U\_p.c) is a C file that contains routines equivalent to those in the client stub and server stub files of an object (COM) interface.</span></span> <span data-ttu-id="f025a-106">Esse arquivo contém implementações das rotinas substitutas para o cliente e o servidor no modo embutido do compilador ou dados equivalentes e conversões nos modos interpretados, bem como outros dados de cola COM apropriados, como o proxy e o stub vtables.</span><span class="sxs-lookup"><span data-stu-id="f025a-106">This file contains implementations of the surrogate routines for client and server in the inline mode of the compiler or equivalent data and thunks in the interpreted modes, as well as other appropriate COM glue data, such as the proxy and stub Vtables.</span></span>

<span data-ttu-id="f025a-107">O arquivo de proxy de interface inclui as rotinas de suporte e os dados somente para métodos das interfaces definidas no arquivo IDL atual.</span><span class="sxs-lookup"><span data-stu-id="f025a-107">The interface proxy file includes the supporting routines and data only for methods of the interfaces defined in the current IDL file.</span></span> <span data-ttu-id="f025a-108">Para esclarecer esse comportamento, um exemplo estendido é usado em toda esta seção.</span><span class="sxs-lookup"><span data-stu-id="f025a-108">To clarify this behavior, an extended example is used throughout this section.</span></span> <span data-ttu-id="f025a-109">Ao compilar um arquivo IDL com uma interface como IFaceB que herda de IFaceA, IFaceB dados auxiliares relacionados e rotinas são gerados para o arquivo de proxy atual, enquanto a interface base IFaceA relacionadas a dados auxiliares e rotinas são encontradas no proxy gerado a partir do arquivo IDL que contém a definição de IFaceA.</span><span class="sxs-lookup"><span data-stu-id="f025a-109">When compiling an IDL file with an interface such as IFaceB that inherits from IFaceA, IFaceB related auxiliary data and routines are generated to the current proxy file, while the base interface IFaceA related auxiliary data and routines are found in the proxy generated from the IDL file containing the IFaceA definition.</span></span> <span data-ttu-id="f025a-110">O compilador gera todos os dados necessários para identificar os substitutos da interface base e delegá-los quando necessário para dar suporte aos métodos IFaceA usados por meio da interface IFaceB.</span><span class="sxs-lookup"><span data-stu-id="f025a-110">The compiler generates all data necessary to identify the surrogates of the base interface, and to delegate to them when needed to support the IFaceA methods used through IFaceB interface.</span></span>

<span data-ttu-id="f025a-111">Para cada método em uma interface no arquivo IDL atual, o arquivo de proxy contém os dois métodos substitutos a seguir quando compilados no modo misto ([/os](-os.md)) e dados de intérprete equivalentes quando compilados no modo de intérprete ([/Oi](-oi.md)).</span><span class="sxs-lookup"><span data-stu-id="f025a-111">For every method in an interface in the current IDL file, the proxy file contains the following two surrogate methods when compiled in the mixed mode ([/Os](-os.md)), and equivalent interpreter data when compiled in the interpreter mode ([/Oi](-oi.md)).</span></span>

-   <span data-ttu-id="f025a-112">O substituto do lado do cliente, como o \_ proxy do método IFaceB \_ neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="f025a-112">The client-side surrogate, such as IFaceB\_Method\_Proxy in this example.</span></span>

    <span data-ttu-id="f025a-113">Esse substituto do lado do cliente é o ponto de entrada virtual para o qual o cliente, por exemplo, IFaceB:: Method, expedetions.</span><span class="sxs-lookup"><span data-stu-id="f025a-113">This client-side surrogate is the virtual entry point to which the client, for example IFaceB::Method, dispatches.</span></span> <span data-ttu-id="f025a-114">Ele realiza marshaling dos argumentos de entrada em um formulário de transmissãotable, transmite os argumentos marshaled com informações que identificam a interface e a operação e, em seguida, desempacota o valor de retorno e quaisquer argumentos de saída quando a operação invocada retorna.</span><span class="sxs-lookup"><span data-stu-id="f025a-114">It marshals the input arguments into a transmittable form, transmits the marshaled arguments along with information that identifies the interface and the operation, and then unmarshals the return value and any output arguments when the invoked operation returns.</span></span>

-   <span data-ttu-id="f025a-115">O substituto do lado do servidor, por exemplo, o \_ stub do método IFaceB \_ .</span><span class="sxs-lookup"><span data-stu-id="f025a-115">The server-side surrogate, for example, IFaceB\_Method\_Stub .</span></span>

    <span data-ttu-id="f025a-116">Esse substituto do lado do servidor é o ponto de entrada virtual que o tempo de execução subjacente despacha para o servidor para emular o cliente.</span><span class="sxs-lookup"><span data-stu-id="f025a-116">This server-side surrogate is the virtual entry point that the underlying runtime dispatches to at the server to emulate the client.</span></span> <span data-ttu-id="f025a-117">Ele desempacota os argumentos de entrada para replicar os dados do cliente, invoca a implementação do servidor da função de interface e, em seguida, realiza o marshaling e transmite o valor de retorno e todos os argumentos de saída para o lado do cliente.</span><span class="sxs-lookup"><span data-stu-id="f025a-117">It unmarshals the input arguments to replicate the client data, invokes the server's implementation of the interface function, and then marshals and transmits the return value and any output arguments back to the client side.</span></span>

<span data-ttu-id="f025a-118">O nome padrão de um arquivo de proxy gerado a partir de um arquivo. idl é \_ o arquivo p. c. Use a opção de compilador [**/proxy nomedearquivo**](-proxy.md) MIDL para substituir o nome padrão do arquivo de proxy da interface.</span><span class="sxs-lookup"><span data-stu-id="f025a-118">The default name for a proxy file generated from a file.idl is file\_p.c.Use the [**/proxy**](-proxy.md) MIDL compiler switch to override the default name of the interface proxy file.</span></span> <span data-ttu-id="f025a-119">As opções [**/env**](-env.md) e [**/out**](-out.md) afetam esse arquivo.</span><span class="sxs-lookup"><span data-stu-id="f025a-119">The [**/env**](-env.md) and [**/out**](-out.md) switches affect this file.</span></span>

 

 




