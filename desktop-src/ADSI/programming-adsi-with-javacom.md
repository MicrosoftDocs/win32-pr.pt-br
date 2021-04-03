---
title: Programando ADSI com Java/COM
description: Usando a máquina virtual da Microsoft para Java (Microsoft VM) e o compilador do Microsoft Java, você tem acesso a todos os recursos ADSI expostos por meio de qualquer componente COM do ADSI, de um aplicativo Java/COM.
ms.assetid: eda516b6-0f89-464f-a9d2-9bb4ca70fda5
ms.tgt_platform: multiple
keywords:
- Programando ADSI com o AD do Java/COM
- ADSI ADSI, usando a programação Java/COM para
- ADSI ADSI, código de exemplo Java
- ADSI ADSI, exemplo de código Java, associando a um objeto ADSI e invocando métodos nesse objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6899804208f9899823f266bc941bcf3c2dec372
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822193"
---
# <a name="programming-adsi-with-javacom"></a>Programando ADSI com Java/COM

Usando a máquina virtual da Microsoft para Java (Microsoft VM) e o compilador do Microsoft Java, você tem acesso a todos os recursos ADSI expostos por meio de qualquer componente COM do ADSI, de um aplicativo Java/COM. O exemplo de código Java a seguir mostra os elementos necessários para associar a um objeto ADSI e invocar métodos nesse objeto. As funções de API ADSI necessárias e os métodos de objeto são expostos por meio de Activeds.dll.


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



O argumento na primeira instrução **Import** refere-se às classes de wrapper Java empacotadas no Activeds.dll. Use o Visual J++ para criar as classes de wrapper e incluí-las em seu projeto, seguindo o procedimento abaixo.

**Para criar classes de wrapper e incluí-las em seu projeto**

1.  Em um projeto do Visual J++, selecione **Adicionar wrapper com...** no menu do **projeto** .
2.  Selecione "biblioteca de tipos do Active DS" nos **componentes instalados:** na caixa de diálogo wrappers com. Se a biblioteca de tipos não for mostrada na caixa de listagem, clique no botão **procurar...** , navegue até o diretório onde activeds. tlb está armazenado e, em seguida, selecione a biblioteca de tipos.

O Visual J++ cria o pacote activeds para as classes de wrapper Java e inclui o pacote no caminho padrão do projeto. Para obter mais informações, consulte o pacote activeds no painel **explorar do projeto** na janela do Visual J++.

Para obter um objeto ADSI que não pode ser Cocriado, use uma das funções de API ADSI expostas, por exemplo, [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) ou [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject), que também são empacotadas em Activeds.dll. O Microsoft J/Direct fornece acesso a essas e a outras APIs nativas. Isso é ilustrado pelas duas últimas linhas do exemplo de código acima.

Ao compilar, verifique se a extensão de idioma da Microsoft está habilitada. Para fazer isso, selecione **<project> Propriedades...** no menu **projeto** na janela do projeto do Visual J++. Em seguida, clique na guia **Compilar** na caixa de diálogo **<project> Propriedades** . Desmarque a caixa de seleção **desabilitar extensões de idioma da Microsoft** . Se estiver compilando na linha de comando, use a opção "/x-", por exemplo:

**JVC/x-SimpleADSI. java**

Por fim, para que a máquina virtual carregue o componente COM, a DLL (biblioteca de vínculo dinâmico) deve estar visível no caminho do sistema. Se um erro "Java. lang. UnsatisfiedLinkError" for retornado, defina o caminho para incluir o caminho que contém a DLL necessária. Por exemplo, se Activeds.dll tiver sido instalado em c: \\ ADSI \\ lib, emita o seguinte comando na linha de comando:

**Definir caminho =% PATH%; c: \\ ADSI \\ lib**

 

 




