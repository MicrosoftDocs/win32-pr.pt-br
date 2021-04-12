---
title: Arquivo de extensão de serviço da Web
description: Esta seção descreve o arquivo de extensão de serviço da Web.
ms.assetid: 856d4ff5-2292-4d87-ae7c-19b100fd1cb3
keywords:
- Serviços Web de arquivo de extensão de serviço da Web para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0802e31895aa5dd5051c94746e774033a1ebe677
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104294619"
---
# <a name="web-service-extension-file"></a><span data-ttu-id="8c69a-106">Arquivo de extensão de serviço da Web</span><span class="sxs-lookup"><span data-stu-id="8c69a-106">Web Service Extension File</span></span>

<span data-ttu-id="8c69a-107">Esta seção descreve o arquivo de extensão de serviço da Web.</span><span class="sxs-lookup"><span data-stu-id="8c69a-107">This section outlines Web Service extension file.</span></span>


<span data-ttu-id="8c69a-108">O arquivo WSX (extensão do serviço WCF) é o nosso arquivo de extensão para permitir que o aplicativo manipule comportamentos locais que não afetam a representação de dados de transmissão.</span><span class="sxs-lookup"><span data-stu-id="8c69a-108">WSX file (WCF service extension) is our extension file to allow application to manipulate local behaviors that do not affect wire data representation.</span></span> <span data-ttu-id="8c69a-109">Deve ser extensível para que possamos adicionar novos recursos no futuro sem interromper a interoperabilidade.</span><span class="sxs-lookup"><span data-stu-id="8c69a-109">It should be extensible that we can add new features in the future without breaking interoperability.</span></span>

<span data-ttu-id="8c69a-110">A estrutura geral de WSX imitaria a estrutura do arquivo XSD ou WSDL, que é um arquivo XML que mantém a mesma estrutura que o arquivo de entrada principal.</span><span class="sxs-lookup"><span data-stu-id="8c69a-110">The overall structure of WSX would mimic the structure of XSD or WSDL file, which is a XML file that maintains the same structure as the main input file.</span></span> <span data-ttu-id="8c69a-111">Atributos extras no mesmo token nomeado no arquivo principal especificariam os atributos que o aplicativo deseja controlar sobre o comportamento padrão.</span><span class="sxs-lookup"><span data-stu-id="8c69a-111">Extra attributes on the same named token in main file would specify the attributes that application wants to control over the default behavior.</span></span>

<span data-ttu-id="8c69a-112">Talvez não faça nada aqui em m3.</span><span class="sxs-lookup"><span data-stu-id="8c69a-112">We might not do anything here in M3.</span></span> <span data-ttu-id="8c69a-113">Na V1, posso ver que damos suporte aos seguintes atributos:</span><span class="sxs-lookup"><span data-stu-id="8c69a-113">In V1, I can see we support the following attributes:</span></span>

<span data-ttu-id="8c69a-114">Uso especificando o campo de argumento/parâmetro de contagem.</span><span class="sxs-lookup"><span data-stu-id="8c69a-114">Usage Specifying count argument/parameter field.</span></span>

<span data-ttu-id="8c69a-115">Este é um atributo de elemento, mas aplicável somente ao tipo de matriz.</span><span class="sxs-lookup"><span data-stu-id="8c69a-115">This is an element attribute but applicable to array type only.</span></span> <span data-ttu-id="8c69a-116">O atributo IsCountOf especifica o elemento da matriz.</span><span class="sxs-lookup"><span data-stu-id="8c69a-116">IsCountOf attribute specifies the array element.</span></span> <span data-ttu-id="8c69a-117">O parâmetro/campo de contagem não aparece em fio.</span><span class="sxs-lookup"><span data-stu-id="8c69a-117">The count field/parameter does not appear on wire.</span></span>

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <element name="FooInParam">
  <complexType> 
   <!-- MyArray field is presented in WSDL file as an element -->
    <element name="MyArrayCount" IsCountOf="MyArray"></element>
   </complexType>
  </element>
 </xs:schema>
```

<span data-ttu-id="8c69a-118">Especificando o retorno de chamada de leitura/gravação para o tipo personalizado</span><span class="sxs-lookup"><span data-stu-id="8c69a-118">Specifying read/write callback for custom type</span></span>

<span data-ttu-id="8c69a-119">Esses atributos forçam wsutil.exe a gerar o [**\_ \_ tipo personalizado WS**](/windows/desktop/api/WebServices/ne-webservices-ws_type) para o tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="8c69a-119">These attributes force wsutil.exe to generate [**WS\_CUSTOM\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_type) for specified type.</span></span> <span data-ttu-id="8c69a-120">\_o atributo ReadCallback personalizado especifica a rotina de [**retorno de chamada de leitura**](/windows/desktop/api/WebServices/nc-webservices-ws_read_type_callback) e WriteCallback personalizado \_ especifica a rotina de [**retorno de chamada de gravação**](/windows/desktop/api/WebServices/nc-webservices-ws_write_type_callback) .</span><span class="sxs-lookup"><span data-stu-id="8c69a-120">custom\_readcallback attribute specifies the [**read callback**](/windows/desktop/api/WebServices/nc-webservices-ws_read_type_callback) routine, and custom\_writecallback specifies the [**write callback**](/windows/desktop/api/WebServices/nc-webservices-ws_write_type_callback) routine.</span></span>

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <element name="mytype" custom_readcallback="myreadcallback" custom_writecallback="mywritecallback"> 
 </element>
</xs:schema>
```

<span data-ttu-id="8c69a-121">Podemos ter um arquivo WSX correspondente para descrever seu comportamento local:</span><span class="sxs-lookup"><span data-stu-id="8c69a-121">We can have a matching WSX file to describe its local behavior:</span></span>

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">

 <element name="FooInParam" DataValidationRoutine="MyArrayValidation">
  <complexType> 
   <element name="MyLocalArrayCount" IsCountOf="MyArray"></element> 
  </complexType>
 </element>
</xs:schema>
```

<span data-ttu-id="8c69a-122">WsUtil.exe gera o seguinte protótipo para a estrutura:</span><span class="sxs-lookup"><span data-stu-id="8c69a-122">WsUtil.exe generates the following prototype for the structure:</span></span>

``` syntax
typedef struct FooInParam
{
  ULONG MyLocalArrayCount;
  int * MyArray;
};
```

 

 




