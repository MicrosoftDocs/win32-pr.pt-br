---
title: Anatomia de um arquivo IDL
description: Esses arquivos IDL de exemplo demonstram as construções fundamentais da definição de interface.
ms.assetid: 9c276b8a-5342-4c09-91a7-c9a9f0f83c73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acbcfbf5c145a1fb389cc26543cf75d8cc75a107
ms.sourcegitcommit: 5ebaf3a456bc68cd0c6bd46c8135b67b1bf6fa54
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "104297851"
---
# <a name="anatomy-of-an-idl-file"></a>Anatomia de um arquivo IDL

Esses arquivos IDL de exemplo demonstram as construções fundamentais da definição de interface. Alocação de memória, marshaling personalizado e mensagens assíncronas são apenas alguns dos recursos que podem ser implementados em uma interface COM personalizada. Os atributos MIDL são usados para definir interfaces COM. Para obter mais informações sobre como implementar interfaces e bibliotecas de tipos, incluindo um resumo de atributos MIDL, consulte [definições de interface e bibliotecas de tipos](/windows/desktop/Midl/interface-definitions-and-type-libraries) no guia e referência do programador de MIDL. Para obter uma referência completa de todos os atributos de MIDL, palavras-chave e diretivas, consulte a [referência de linguagem MIDL](/windows/desktop/Midl/midl-language-reference).

## <a name="exampleidl"></a>Exemplo de IDL

O arquivo IDL de exemplo a seguir define duas interfaces COM. Nesse arquivo IDL, Midl.exe gerará proxy/stub e arquivos de cabeçalho e código de marshaling. Uma desseção linha por linha segue o exemplo.

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

A instrução de [**importação**](/windows/desktop/Midl/import) de IDL é usada aqui para trazer um arquivo de cabeçalho, Mydefs. h, que contém tipos definidos pelo usuário e Unknwn. idl, que contém a definição de [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), da qual IFace1 e IFace2 derivam.

O atributo [**Object**](/windows/desktop/Midl/object) identifica a interface como uma interface de objeto e informa ao compilador MIDL para gerar código de proxy/stub em vez de stubs de cliente e de servidor RPC. Os métodos de interface de objeto devem ter um tipo de retorno de [**HRESULT**](/openspecs/windows_protocols/ms-erref/0642cb2f-2075-4469-918c-4441e69c548a), para permitir que o mecanismo RPC subjacente Relate erros para chamadas que não foram concluídas devido a problemas de rede.

O atributo [**UUID**](/windows/desktop/Midl/uuid) especifica o identificador de interface (IID). Cada interface, classe e biblioteca de tipos deve ser identificada com seu próprio identificador exclusivo. Use o Uuidgen.exe do utilitário para gerar um conjunto de IDs exclusivos para suas interfaces e outros componentes.

A palavra-chave [**interface**](/windows/desktop/Midl/interface) define o nome da interface. Todas as interfaces de objeto devem derivar, direta ou indiretamente, de [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown).

O [**parâmetro direcional especifica**](/windows/desktop/Midl/in) um parâmetro que é definido somente pelo chamador. O parâmetro [**out**](/windows/desktop/Midl/out-idl) especifica os dados que são passados de volta para o chamador. O uso de ambos os atributos direcionais em um parâmetro especifica que o parâmetro é usado para enviar dados para o método e para passar dados de volta para o chamador.

O [**atributo \_ padrão de ponteiro**](/windows/desktop/Midl/pointer-default) especifica o tipo de ponteiro padrão ([**Unique**](/windows/desktop/Midl/unique), [**ref**](/windows/desktop/Midl/ref)ou [**PTR**](/windows/desktop/Midl/ptr)) para todos os ponteiros, exceto aqueles incluídos nas listas de parâmetros. Se nenhum tipo padrão for especificado, MIDL assumirá que ponteiros únicos são **exclusivos**. No entanto, quando você tem vários níveis de ponteiros, deve especificar explicitamente um tipo de ponteiro padrão, mesmo se desejar que o tipo padrão seja **exclusivo**.

No exemplo anterior, a matriz BkfstStuff \[ \] é uma *matriz compatível*, cujo tamanho é determinado em tempo de execução. O atributo [**Max \_ is**](/windows/desktop/Midl/max-is) especifica a variável que contém o valor máximo para o índice de matriz.

O atributo [**Size \_ também é**](/windows/desktop/Midl/size-is) usado para especificar o tamanho de uma matriz ou, como no exemplo anterior, vários níveis de ponteiros. No exemplo, a chamada pode ser feita sem saber com antecedência a quantidade de dados que será retornada.

## <a name="example2idl"></a>Example2. idl

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

O atributo [**HelpString**](/windows/desktop/Midl/helpstring) é opcional; Você o usa para descrever brevemente o objeto ou para fornecer uma linha de status. Essas cadeias de caracteres de ajuda são legíveis com um pesquisador de objetos, como aquele fornecido com o Microsoft Visual Basic.

O atributo [**Dual**](/windows/desktop/Midl/dual) no IFace3 cria uma interface que é uma interface de expedição e uma interface com. Como ele é derivado de **IDispatch**, uma interface dupla dá suporte à automação, que é o que o atributo [**oleautomation**](/windows/desktop/Midl/oleautomation) especifica. IFace3 importa Oaidl. idl para obter a definição de **IDispatch**.

A instrução [**library**](/windows/desktop/Midl/library) define a biblioteca de tipos ExampleLib, que tem seus próprios atributos [**UUID**](/windows/desktop/Midl/uuid), [**HelpString**](/windows/desktop/Midl/helpstring)e [**version**](/windows/desktop/Midl/version) .

Dentro da definição da biblioteca de tipos, a diretiva [**importlib**](/windows/desktop/Midl/importlib) coloca em uma biblioteca de tipos compilada. Todas as definições de biblioteca de tipos devem trazer a biblioteca de tipos base definida em Stdole32. tlb.

Essa definição de biblioteca de tipos demonstra três maneiras diferentes de incluir interfaces na biblioteca de tipos. IFace3 é incluído meramente referenciando-o dentro da instrução da biblioteca.

A instrução [**coclass**](/windows/desktop/Midl/coclass) define uma classe de componente totalmente nova, BkfstComponent, que inclui duas interfaces definidas anteriormente, IFace1 e IFace2. O atributo padrão designa IFace1 como a interface padrão.

IFace4 é descrito dentro da instrução de biblioteca. O atributo [**propput**](/windows/desktop/Midl/propput) em methoded indica que o método executa uma ação set em uma propriedade de mesmo nome. O atributo [**propget**](/windows/desktop/Midl/propget) indica que o método recupera informações de uma propriedade de mesmo nome que o método. O atributo [**retval**](/windows/desktop/Midl/retval) em methoded designa um parâmetro de saída que contém o valor de retorno da função.

 

 
