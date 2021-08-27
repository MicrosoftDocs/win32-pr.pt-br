---
title: Programando ADSI com Java/COM
description: Usando a máquina virtual da Microsoft para Java (VM da Microsoft) e o Compilador Java da Microsoft, você tem acesso a todos os recursos ADSI expostos por meio de qualquer componente COM ADSI, de um aplicativo Java/COM.
ms.assetid: eda516b6-0f89-464f-a9d2-9bb4ca70fda5
ms.tgt_platform: multiple
keywords:
- Programando ADSI com Java/COM AD
- ADSI ADSI , usando programação Java/COM para
- ADSI ADSI , código de exemplo Java
- ADSI ADSI , código de exemplo Java , associação a um objeto ADSI e invocação de métodos nesse objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aec873822d27a7b5fcf95aad7c31a8978552eb88
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880296"
---
# <a name="programming-adsi-with-javacom"></a>Programando ADSI com Java/COM

Usando a máquina virtual da Microsoft para Java (VM da Microsoft) e o Compilador Java da Microsoft, você tem acesso a todos os recursos ADSI expostos por meio de qualquer componente COM ADSI, de um aplicativo Java/COM. O exemplo de código Java a seguir mostra os elementos necessários para se vincular a um objeto ADSI e invocar métodos nesse objeto. As funções e os métodos de objeto da API ADSI necessários são expostos por meio de Activeds.dll.


```C++
import activeds.*;       // ADSI COM Wrapper classes
import com.ms.com.*;     // to use _Guid data type in COM.

public Class SimpleADSI 
{
    IADs obj;
    String path = "WinNT://domain/machine,computer";
    _Guid riid = IADs.iid;
    public static void main(String args[]) 
    {
        try 
        {
            obj = (IADs)ADsGetObject(path, riid);
            System.out.println( "Object name:  " + obj.getName() );
            System.out.println( "      class:  " + obj.getSchema() );
            System.out.println( "    ADsPath:  " + obj.getADsPath() );
            System.out.println( "     parent:  " + obj.getParent() );
        }
        catch (Exception e) 
        {
            System.out.println( "SimpleADSI Error: " + e.toString() );
        }
    }

    /** @dll.import("activeds", ole) */
    private static native IUnknown ADsGetObject(String path, _Guid riid);
}
```



O argumento na primeira **instrução de importação** refere-se a classes de Wrapper Java empacotados em Activeds.dll. Use o Visual J++ para criar as classes de wrapper e incluí-las em seu projeto, seguindo o procedimento abaixo.

**Para criar classes de wrapper e incluí-las em seu projeto**

1.  Em um projeto do Visual J++, **selecione Adicionar Wrapper com...** no menu **Project.**
2.  Selecione "Active DS Type Library" na caixa de diálogo **Componentes Instalados:** na caixa de diálogo Wrappers COM. Se a biblioteca de tipos não for mostrada na caixa de listagem, clique no botão **Procurar...,** navegue até o diretório em que Activeds.tlb está armazenado e selecione a biblioteca de tipos.

O Visual J++ cria o pacote activeds para as classes do Java Wrapper e inclui o pacote no caminho padrão do projeto. Para obter mais informações, consulte o pacote activeds **no painel Project Explorar** na janela do Visual J++.

Para obter um objeto ADSI que não pode ser cocriado, use uma das funções de API ADSI expostas, por exemplo, [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) ou [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject), que também são empacotadas em Activeds.dll. O Microsoft J/Direct fornece acesso a essas e outras APIs nativas. Isso é ilustrado pelas duas últimas linhas do exemplo de código acima.

Ao compilar, verifique se a Extensão de Linguagem da Microsoft está habilitada. Para fazer isso, selecione **&lt; Propriedades do &gt; projeto...** no menu **Project** na janela do projeto do Visual J++. Em seguida, clique na **guia Compilar** na caixa **&lt; de diálogo Propriedades &gt; do** projeto. Des marque **a caixa de seleção Desabilitar Extensões de Linguagem** da Microsoft. Se estiver compilando da linha de comando, use a opção "/x-", por exemplo:

**jvc /x- SimpleADSI.java**

Por fim, para que a máquina virtual carregue o componente COM, a DLL (biblioteca de vínculo dinâmico) deve estar visível no caminho do sistema. Se um erro "java.lang.UnsatisfiedLinkError" for retornado, de definir o CAMINHO para incluir o caminho que contém a DLL necessária. Por exemplo, se Activeds.dll foi instalado em c: adsi lib, em seguida, em um \\ comando da linha de \\ comando:

**set PATH = %PATH%; c: \\ adsi \\ lib**

 

 




