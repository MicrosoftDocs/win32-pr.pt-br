---
title: Acessando serviços usando Java
description: Acessando serviços usando Java
ms.assetid: 3eced858-487a-4f36-a7a1-34ac827aad13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c24ae7508b5999e5d07f2480d49cb4c20dd89a0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917210"
---
# <a name="accessing-services-using-java"></a><span data-ttu-id="e4c28-103">Acessando serviços usando Java</span><span class="sxs-lookup"><span data-stu-id="e4c28-103">Accessing Services Using Java</span></span>

<span data-ttu-id="e4c28-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e4c28-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="e4c28-105">Você também pode acessar os serviços do Microsoft Agent por meio de um miniaplicativo Java.</span><span class="sxs-lookup"><span data-stu-id="e4c28-105">You can also access Microsoft Agent services from a Java applet.</span></span> <span data-ttu-id="e4c28-106">Muitas das funções acessíveis por meio das interfaces do Microsoft Agent retornam valores por meio de parâmetros passados por referência.</span><span class="sxs-lookup"><span data-stu-id="e4c28-106">Many of the functions accessible through the Microsoft Agent interfaces return values through parameters passed by reference.</span></span> <span data-ttu-id="e4c28-107">Para passar esses parâmetros do Java, é necessário criar matrizes de elemento único em seu código e passá-las como parâmetros para a função apropriada.</span><span class="sxs-lookup"><span data-stu-id="e4c28-107">In order to pass these parameters from Java, it is necessary to create single-element arrays in your code and pass them as parameters to the appropriate function.</span></span> <span data-ttu-id="e4c28-108">Se você estiver usando o Microsoft Visual J++ e tiver executado o assistente do Java Type Library no servidor do Microsoft Agent, consulte o arquivo summary.txt para revisar quais funções exigem argumentos de matriz.</span><span class="sxs-lookup"><span data-stu-id="e4c28-108">If you are using Microsoft Visual J++ and have run the Java Type Library Wizard on the Microsoft Agent server, refer to the summary.txt file to review which functions require array arguments.</span></span> <span data-ttu-id="e4c28-109">O procedimento é semelhante ao de C; Use a interface [**IAgentEx**](https://www.bing.com/search?q=**IAgentEx**) para criar uma instância do servidor e, em seguida, carregue o caractere:</span><span class="sxs-lookup"><span data-stu-id="e4c28-109">The procedure is similar to that in C; you use the [**IAgentEx**](https://www.bing.com/search?q=**IAgentEx**) interface to create an instance of the server, then load the character:</span></span>


```
private IAgentEx            m_AgentEx = null;
private IAgentCharacterEx   m_Merlin[] = {null};
private int                 m_MerlinID[] = {-1};
private int                 m_RequestID[] = {0};
private final String        m_CharacterPath = "merlin.acs";

public void start()
{
      // Start the Microsoft Agent Server

      m_AgentEx = (IAgentEx) new AgentServer();

      try
      {

         Variant characterPath = new Variant();
         characterPath.putString(m_CharacterPath);

         // Load the character

         m_AgentEx.Load(characterPath,
                    m_MerlinID,
                    m_RequestID);
      }
```



<span data-ttu-id="e4c28-110">O procedimento é um pouco diferente ao carregar caracteres de um local remoto HTTP, como um site.</span><span class="sxs-lookup"><span data-stu-id="e4c28-110">The procedure is slightly different when loading characters from a HTTP remote location such as a website.</span></span> <span data-ttu-id="e4c28-111">Nesse caso, o método [**Load**](/previous-versions/visualstudio/foxpro/h1tx7zt1(v=vs.71)) é assíncrono e gerará uma exceção com de E \_ pendente (0x8000000a).</span><span class="sxs-lookup"><span data-stu-id="e4c28-111">In this case the [**Load**](/previous-versions/visualstudio/foxpro/h1tx7zt1(v=vs.71)) method is asynchronous and will raise a COM exception of E\_PENDING (0x8000000a).</span></span> <span data-ttu-id="e4c28-112">Você precisará capturar essa exceção e tratá-la corretamente, como é feito nas seguintes funções:</span><span class="sxs-lookup"><span data-stu-id="e4c28-112">You will need to catch this exception and handle it correctly as is done in the following functions:</span></span>


```
// Constants used in asynchronous character loads

private final int E_PENDING = 0x8000000a;
private final int NOERROR = 0;


// This function loads a character from the specified path.
// It correctly handles the loading of characters from
// remote sites.

// This sample doesn't care about the request id returned
// from the Load call.  Real production code might use the
// request id and the RequestComplete callback to check for
// a successful character load before proceeding.

public int LoadCharacter(Variant path, int[] id)
{
   int requestid[] = {-1};
   int hRes = 0;

   try
   {
      // Load the character

      m_AgentEx.Load(path, id, requestid);
   }
   catch(com.ms.com.ComException e)
   {
      // Get the HRESULT

      hRes = e.getHResult();
      
      // If the error code is E_PENDING, we return NOERROR

      if (hRes == E_PENDING)
         hRes = NOERROR;
   }

   return hRes;
}

public void start()
{
   if (LoadCharacter(characterPath, m_MerlinID) != NOERROR)
   {
      stop();
      return;
   }

   // Other initialization code here

   .
   .
   .
}
```



<span data-ttu-id="e4c28-113">Em seguida, obtenha a interface [**IAgentCharacterEx**](https://www.bing.com/search?q=**IAgentCharacterEx**) que permite que você acesse seus métodos:</span><span class="sxs-lookup"><span data-stu-id="e4c28-113">Then get the [**IAgentCharacterEx**](https://www.bing.com/search?q=**IAgentCharacterEx**) interface that enables you to access its methods:</span></span>


```
// Get the IAgentCharacterEx interface for the loaded
// character by passing its ID to the Agent server.

m_AgentEx.GetCharacterEx(m_MerlinID[0], m_Merlin);

// Show the character

m_Merlin[0].Show(FALSE, m_RequestID);

// And speak hello

m_Merlin[0].Speak("Hello World!", "", m_RequestID);
```



<span data-ttu-id="e4c28-114">Da mesma forma, para ser notificado de eventos, você deve implementar a interface [**IAgentNotifySink**](https://www.bing.com/search?q=**IAgentNotifySink**) ou [**IAgentNotifySinkEx**](https://www.bing.com/search?q=**IAgentNotifySinkEx**) , criando e registrando um objeto desse tipo:</span><span class="sxs-lookup"><span data-stu-id="e4c28-114">Similarly, to be notified of events, you must implement either the [**IAgentNotifySink**](https://www.bing.com/search?q=**IAgentNotifySink**) or the [**IAgentNotifySinkEx**](https://www.bing.com/search?q=**IAgentNotifySinkEx**) interface, creating and registering an object of that type:</span></span>


```
...
// Declare an Agent Notify Sink so that we can get
// notification callbacks from the Agent server.

private AgentNotifySinkEx m_SinkEx = null;
private int            m_SinkID[] = {-1};

public void start()
   {
   ...
   // Create and register a notify sink

   m_SinkEx = new AgentNotifySinkEx();

   m_AgentEx.Register(m_SinkEx, m_SinkID);
   …
   // Give our notify sink access to the character

   m_SinkEx.SetCharacter(m_Merlin[0]);
   ...
   }
```



<span data-ttu-id="e4c28-115">Para acessar o Microsoft Agent a partir de um miniaplicativo Java, você deve gerar classes Java que você instala com o applet.</span><span class="sxs-lookup"><span data-stu-id="e4c28-115">In order to access Microsoft Agent from a Java applet, you must generate Java classes that you install with the applet.</span></span> <span data-ttu-id="e4c28-116">Você pode usar o assistente de biblioteca de tipos Java do Visual J++, por exemplo, para gerar esses arquivos.</span><span class="sxs-lookup"><span data-stu-id="e4c28-116">You can use the Visual J++ Java Type Library Wizard, for example, to generate these files.</span></span> <span data-ttu-id="e4c28-117">Se você planeja hospedar o applet em uma página da Web, será necessário criar um CAB Java assinado incluindo os arquivos de classe gerados que são baixados com a página.</span><span class="sxs-lookup"><span data-stu-id="e4c28-117">If you plan to host the applet on a webpage, you will need to build a signed Java CAB inclusive of the generated class files that download with the page.</span></span> <span data-ttu-id="e4c28-118">Os arquivos de classe são necessários para acessar o servidor do Microsoft Agent, pois ele é um objeto COM, que é executado fora da área restrita do Java.</span><span class="sxs-lookup"><span data-stu-id="e4c28-118">The class files are necessary to access the Microsoft Agent Server since it is a COM object, that executes outside of the Java sandbox.</span></span> <span data-ttu-id="e4c28-119">Para saber mais sobre a segurança de Trust-Based para Java, consulte <https://www.microsoft.com/java/security> .</span><span class="sxs-lookup"><span data-stu-id="e4c28-119">To learn more about Trust-Based Security for Java, see <https://www.microsoft.com/java/security>.</span></span>

 

 