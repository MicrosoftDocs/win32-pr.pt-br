---
title: Anatomia de um arquivo IDL
description: Esses arquivos IDL de exemplo demonstram os constructos fundamentais da definição de interface.
ms.assetid: 9c276b8a-5342-4c09-91a7-c9a9f0f83c73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 531d46bfcfa0ef4e4eee075ae65b64dd0c80a8f6a51543a1762a0ddcd8a03888
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118311330"
---
# <a name="anatomy-of-an-idl-file"></a>Anatomia de um arquivo IDL

Esses arquivos IDL de exemplo demonstram os constructos fundamentais da definição de interface. Alocação de memória, marshaling personalizado e mensagens assíncronas são apenas alguns dos recursos que você pode implementar em uma interface COM personalizada. Atributos MIDL são usados para definir interfaces COM. Para obter mais informações sobre como implementar interfaces e bibliotecas de tipos, incluindo um resumo dos atributos MIDL, consulte Definições de interface e [bibliotecas](/windows/desktop/Midl/interface-definitions-and-type-libraries) de tipos no Guia e referência do programador MIDL. Para uma referência completa de todos os atributos, palavras-chave e diretivas MIDL, consulte a [Referência de linguagem MIDL](/windows/desktop/Midl/midl-language-reference).

## <a name="exampleidl"></a>Example.idl

O arquivo IDL de exemplo a seguir define duas interfaces COM. Desse arquivo IDL, Midl.exe gerará proxy/stub e marshaling de código e arquivos de header. Uma dissecação linha a linha segue o exemplo.

``` syntax
//
// Example.idl 
//
import "mydefs.h","unknwn.idl"; 
[
object,
uuid(a03d1420-b1ec-11d0-8c3a-00c04fc31d2f),
] interface IFace1 : IUnknown
{
HRESULT MethodA([in] short Bread, [out] BKFST * pBToast);
HRESULT MethodB([in, out] BKFST * pBPoptart);
};
 
[
object,
uuid(a03d1421-b1ec-11d0-8c3a-00c04fc31d2f),
pointer_default(unique)
] interface IFace2 : IUnknown
{
HRESULT MethodC([in] long Max,
                [in, max_is(Max)] BkfstStuff[ ],
                [out] long * pSize,
                [out, size_is( , *pSize)] BKFST ** ppBKFST);
}; 
 
```

A instrução [](/windows/desktop/Midl/import) de importação IDL é usada aqui para trazer um arquivo de header, Mydefs.h, que contém tipos definidos pelo usuário e Unknwn.idl, que contém a definição [**de IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), do qual IFace1 e IFace2 derivam.

O [**atributo**](/windows/desktop/Midl/object) de objeto identifica a interface como uma interface de objeto e informa ao compilador MIDL para gerar código proxy/stub em vez de stubs de cliente e servidor RPC. Os métodos de interface de objeto devem ter um tipo de retorno [**HRESULT**](/openspecs/windows_protocols/ms-erref/0642cb2f-2075-4469-918c-4441e69c548a)para permitir que o mecanismo RPC subjacente reporte erros para chamadas que não são concluídas devido a problemas de rede.

O [**atributo uuid**](/windows/desktop/Midl/uuid) especifica o IID (identificador de interface). Cada interface, classe e biblioteca de tipos devem ser identificados com seu próprio identificador exclusivo. Use o utilitário Uuidgen.exe para gerar um conjunto de IDs exclusivas para suas interfaces e outros componentes.

A [**palavra-chave**](/windows/desktop/Midl/interface) interface define o nome da interface. Todas as interfaces de objeto devem derivar, direta ou indiretamente, [**de IUnknown.**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)

O [**parâmetro**](/windows/desktop/Midl/in) direcional em especifica um parâmetro que é definido somente pelo chamador. O [**parâmetro out**](/windows/desktop/Midl/out-idl) especifica os dados que são passados de volta para o chamador. O uso de ambos os atributos direcionais em um parâmetro especifica que o parâmetro é usado para enviar dados para o método e para passar dados de volta para o chamador.

O [**atributo \_ padrão**](/windows/desktop/Midl/pointer-default) do ponteiro especifica o tipo de ponteiro padrão ([**exclusivo,**](/windows/desktop/Midl/unique) [**ref**](/windows/desktop/Midl/ref)ou [**ptr**](/windows/desktop/Midl/ptr)) para todos os ponteiros, exceto aqueles incluídos nas listas de parâmetros. Se nenhum tipo padrão for especificado, MIDL assumirá que os ponteiros únicos são **exclusivos.** No entanto, quando você tiver vários níveis de ponteiros, deverá especificar explicitamente um tipo de ponteiro padrão, mesmo que você queira que o tipo padrão seja **exclusivo.**

No exemplo anterior, a matriz BkfstStuff é uma matriz compatível , o tamanho do qual é \[ \] determinado em tempo de operação.  O [**atributo \_ max is**](/windows/desktop/Midl/max-is) especifica a variável que contém o valor máximo para o índice de matriz.

O [**atributo \_ size**](/windows/desktop/Midl/size-is) é também usado para especificar o tamanho de uma matriz ou, como no exemplo anterior, vários níveis de ponteiros. No exemplo, a chamada pode ser feita sem saber com antecedência quantos dados serão retornados.

## <a name="example2idl"></a>Example2.idl

O exemplo de IDL a seguir (que reutiliza as interfaces descritas no exemplo de IDL anterior) mostra as várias maneiras de gerar informações de biblioteca de tipos para interfaces.

``` syntax
//
// Example2.idl
//

import "example.idl","oaidl.idl"; 

[
uuid(a03d1422-b1ec-11d0-8c3a-00c04fc31d2f),
helpstring("IFace3 interface"),
pointer_default(unique);
dual,
oleautomation
] 
interface IFace3 : IDispatch
{
   HRESULT MethodD([in] BSTR OrderIn,
                   [out, retval] * pTakeOut);
}; //end IFace3 def

[
uuid(a03d1423-b1ec-11d0-8c3a-00c04fc31d2f),
version(1.0),
helpstring("Example Type Library"),
] library ExampleLib
{
  importlib("stdole32.tlb");
  interface IFace3;
  [
  uuid(a03d1424-b1ec-11d0-8c3a-00c04fc31d2f),
  helpstring("Breakfast Component Class")
  ] coclass BkfstComponent
    {
    [default]interface IFace1;
    interfaceIFace2
    }; //end coclass def

[
uuid(a03d1424-b1ec-11d0-8c3a-00c04fc31d2f),
helpstring("IFace4 interface"),
pointer_default(unique);
dual,
oleautomation
] 
interface IFace4 : IDispatch
{
[propput] HRESULT MethodD([in] BSTR OrderIn);
[propget] HRESULT MethodE([out, retval] * pTakeOut);
}; //end IFace4 def
 
}; //end library def
 
```

O [**atributo helpstring**](/windows/desktop/Midl/helpstring) é opcional; você o usa para descrever brevemente o objeto ou para fornecer uma linha de status. Essas cadeias de caracteres de ajuda podem ser lidas com um navegador de objetos, como aquele fornecido com o Microsoft Visual Basic.

O [**atributo**](/windows/desktop/Midl/dual) duplo em IFace3 cria uma interface que é uma interface de expedição e uma interface COM. Como ele é derivado de **IDispatch,** uma interface dupla dá suporte à Automação, que é o que o atributo [**oleautomation**](/windows/desktop/Midl/oleautomation) especifica. IFace3 importa O o odl.idl para obter a definição **de IDispatch**.

A [**instrução**](/windows/desktop/Midl/library) library define a biblioteca de tipos ExampleLib, que tem seus próprios [**atributos uuid,**](/windows/desktop/Midl/uuid) [**helpstring**](/windows/desktop/Midl/helpstring)e [**version.**](/windows/desktop/Midl/version)

Dentro da definição da biblioteca de tipos, a [**diretiva importlib**](/windows/desktop/Midl/importlib) traz uma biblioteca de tipos compilada. Todas as definições de biblioteca de tipos devem trazer a biblioteca de tipos base definida em Stdole32.tlb.

Essa definição de biblioteca de tipos demonstra três maneiras diferentes de incluir interfaces na biblioteca de tipos. IFace3 é incluído apenas referenciando-o na instrução de biblioteca.

A [**instrução coclass**](/windows/desktop/Midl/coclass) define uma classe de componente totalmente nova, BkfstComponent, que inclui duas interfaces definidas anteriormente, IFace1 e IFace2. O atributo padrão designa IFace1 como a interface padrão.

IFace4 é descrito na instrução de biblioteca. O [**atributo propput**](/windows/desktop/Midl/propput) em MethodD indica que o método executa uma ação de conjunto em uma propriedade de mesmo nome. O [**atributo propget**](/windows/desktop/Midl/propget) indica que o método recupera informações de uma propriedade do mesmo nome que o método . O [**atributo retval**](/windows/desktop/Midl/retval) em MethodD designa um parâmetro de saída que contém o valor de retorno da função.

 

 
