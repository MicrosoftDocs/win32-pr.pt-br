---
description: Qualquer aplicativo COM+ pode ser exposto como um serviço Web XML.
ms.assetid: 03c3d5a7-eb98-4916-b6ef-ef6aac86c574
title: Criando Serviços Web XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12dbc5ee08d9300d52b538648ba520b16a60a9e3769242c252eaa40d518a3ea1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118307333"
---
# <a name="creating-xml-web-services"></a>Criando Serviços Web XML

Qualquer aplicativo COM+ pode ser exposto como um serviço Web XML. Os métodos nas interfaces padrão dos componentes configurados aplicativos (componentes no catálogo COM+ de servidores) podem ser chamados remotamente. Você pode usar a ferramenta administrativa serviços de componentes para criar um diretório raiz virtual do IIS a partir do qual os métodos de componente podem ser chamados usando SOAP.

> [!Note]  
> o .NET Framework deve ser instalado em seu computador para expor um aplicativo COM+ como um serviço web XML.

 

**Para expor um aplicativo COM+ como um serviço Web XML**

1.  Na árvore de console da ferramenta administrativa serviços de componentes, em **serviços de componentes**, abra a pasta **aplicativos com+** associada ao computador que você deseja gerenciar.

2.  Clique com o botão direito do mouse no aplicativo que você deseja expor como um serviço Web XML e escolha **Propriedades**.

3.  Clique na guia **ativação** na caixa de diálogo Propriedades.

4.  Marque a caixa de seleção **usa SOAP** .

5.  Na caixa de texto **Vroot do SOAP** , digite o nome do diretório raiz virtual do IIS do qual os métodos dos componentes podem ser acessados remotamente. Observe que uma VRoot SOAP não pode ser um subdiretório de outro diretório VRoot SOAP.

6.  Clique em **OK**.

    Se você especificar o diretório raiz virtual do IIS como *vroot* e se o nome de domínio totalmente qualificado de seus servidores for *ServerName*, a URL em que o componente é exposto como um serviço Web XML é https://*ServerName* / *vroot*/.

    O diretório correspondente no sistema de arquivos é o \\ Windows \\ System32 \\ com \\ SoapVRoots \\ *vroot* \\ ; o COM+ coloca vários arquivos de configuração e ASP.NET programas lá. Para um serviço Web XML sob carga pesada, talvez você queira ajustar os parâmetros armazenados no arquivo web.config. Para obter informações sobre esse arquivo, consulte a documentação do IIS.

    as configurações de segurança padrão para um aplicativo COM+ exposto como um serviço web XML diferem dependendo de qual versão do .NET Framework está instalada. Se a versão 1,0 estiver instalada, os serviços Web XML não serão seguros por padrão; todas as chamadas são aceitas e nenhuma criptografia é usada. Se a versão 1,1 ou posterior estiver instalada, os serviços Web XML serão protegidos por padrão; os chamadores devem ser autenticados e a criptografia é necessária.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Acessando serviços Web XML no modo CAO](accessing-xml-web-services-in-cao-mode.md)
</dt> <dt>

[Acessando serviços Web XML no modo WKO](accessing-xml-web-services-in-wko-mode.md)
</dt> <dt>

[Visão geral do serviço SOAP COM+](com--soap-service-overview.md)
</dt> <dt>

[Protegendo serviços Web XML](securing-xml-web-services.md)
</dt> </dl>

 

 



