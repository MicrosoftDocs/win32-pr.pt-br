---
description: Um objeto SWbemNamedValueSet é uma coleção de objetos SWbemNamedValue.
ms.assetid: 7d1c3a28-d0d3-4108-9628-74ad483e328e
ms.tgt_platform: multiple
title: Objeto SWbemNamedValueSet (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet
- ISWbemNamedValueSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: cfdcc3ba2bde6dfdfd0cc732e4376ceb69ba60904f4d787d9030299c248ebb62
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119732666"
---
# <a name="swbemnamedvalueset-object"></a>Objeto SWbemNamedValueSet

Um objeto **SWbemNamedValueSet** é uma coleção de objetos [**SWbemNamedValue**](swbemnamedvalue.md) . Os métodos e as propriedades de **SWbemNamedValueSet** são usados principalmente para enviar mais informações aos provedores ao enviar determinadas chamadas para o WMI. Todas as chamadas em [**SWbemServices**](swbemservices.md)e algumas chamadas em [**SWbemObject**](swbemobject.md), usam um parâmetro opcional que é um objeto desse tipo. Um cliente pode adicionar informações a um objeto **SWbemNamedValueSet** e enviar o objeto **SWbemNamedValueSet** com a chamada como um dos parâmetros. Esse objeto pode ser criado pela chamada do VBScript **CreateObject** .

Para obter mais informações, consulte [acessando uma coleção](accessing-a-collection.md).

> [!Note]  
> Importante-se possível, não use esse mecanismo porque ele pode interromper o modelo de acesso uniforme que é a base do WMI. Se um provedor usar esse mecanismo, é importante que esse mecanismo seja usado da maneira mais moderada possível. Se um provedor exigir uma grande quantidade de informações de contexto altamente específicas para responder a uma solicitação, todos os clientes deverão ser codificados para fornecer essas informações. Esse mecanismo permite que você acesse provedores, se necessário.

 

Um objeto **SWbemNamedValueSet** é uma coleção de elementos [**SWbemNamedValue**](swbemnamedvalue.md) . Esses itens são adicionados à coleção usando o método [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) . Eles são removidos usando o método [**SWbemNamedValueSet. Remove**](swbemnamedvalueset-remove.md) e recuperados usando o método [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) . Você pode acessar os métodos para preencher qualquer informação de contexto exigida por um provedor dinâmico. Depois de chamar um dos métodos [**SWbemServices**](swbemservices.md) , você pode reutilizar o objeto **SWbemNamedValueSet** para outra chamada.

O provedor subjacente determina as informações contidas em um objeto **SWbemNamedValueSet** . O WMI não faz uso das informações, mas simplesmente a encaminha para o provedor. Os provedores devem publicar as informações de contexto necessárias para atender a solicitações.

## <a name="members"></a>Membros

O objeto **SWbemNamedValueSet** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **SWbemNamedValueSet** tem esses métodos.



| Método                                            | Descrição                                                                                                                              |
|:--------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [**Agrega**](swbemnamedvalueset-add.md)             | Adiciona um objeto [**SWbemNamedValue**](swbemnamedvalue.md) à coleção.<br/>                                                  |
| [**Clone**](swbemnamedvalueset-clone.md)         | Faz uma cópia desta coleção **SWbemNamedValueSet** .<br/>                                                                       |
| [**DeleteAll**](swbemnamedvalueset-deleteall.md) | Remove todos os itens da coleção, tornando o objeto **SWbemNamedValueSet** vazio.<br/>                                        |
| [**Item**](swbemnamedvalueset-item.md)           | Recupera um objeto [**SWbemNamedValue**](swbemnamedvalue.md) da coleção. Esse é o método padrão do objeto.<br/> |
| [**Remover**](swbemnamedvalueset-remove.md)       | Remove um objeto [**SWbemNamedValue**](swbemnamedvalue.md) da coleção.<br/>                                             |



 

### <a name="properties"></a>Propriedades

O objeto **SWbemNamedValueSet** tem essas propriedades.



| Propriedade                                             | Tipo de acesso          | Descrição                                       |
|:-----------------------------------------------------|:---------------------|:--------------------------------------------------|
| [**Contagem**](swbemnamedvalueset-count.md)<br/> | Somente leitura<br/> | Número de itens na coleção.<br/> |



 

## <a name="examples"></a>Exemplos

O exemplo de VBScript a seguir demonstra a manipulação de conjuntos de valores nomeados, no caso de o valor nomeado ser um tipo de matriz.


```VB
Set Context = CreateObject("WbemScripting.SWbemNamedValueSet")

On Error Resume Next

Context.Add "n1", Array (1, 2, 3)
str = "The initial value of n1 is {"
for x=LBound(Context("n1")) to UBound(Context("n1"))
 str = str & Context("n1")(x)
 if x <> UBound(Context("n1")) Then
  str = str & ", "
 End if
next
str = str & "}"
WScript.Echo str

WScript.Echo ""

' report the value of an element of the context value
v = Context("n1")
WScript.Echo "By indirection the first element of n1 has value:",v(0)

' report the value directly
WScript.Echo "By direct access the first element of n1 has value:", Context("n1")(0)

' set the value of a single named value element
Context("n1")(1) = 11 
WScript.Echo "After direct assignment the first element of n1 has value:", Context("n1")(1)

' set the value of a single named value element
Set v = Context("n1")
v(1) = 345
WScript.Echo "After indirect assignment the first element of n1 has value:", Context("n1")(1)

' set the value of an entire context value
Context("n1") = Array (5, 34, 178871)
WScript.Echo "After direct array assignment the first element of n1 has value:", Context("n1")(1)

str = "After direct assignment the entire value of n1 is {"
for x=LBound(Context("n1")) to UBound(Context("n1"))
 str = str & Context("n1")(x)
 if x <> UBound(Context("n1")) Then
  str = str & ", "
 End if
next
str = str & "}"
WScript.Echo str

if Err <> 0 Then
 WScript.Echo Err.Description
 Err.Clear
End if
```



O exemplo do Perl a seguir demonstra a manipulação de conjuntos de valores nomeados, no caso de o valor nomeado ser um tipo de matriz.


```
use strict;
use Win32::OLE;

my ( $Context, $str, $x, @v);

eval {$Context = new Win32::OLE 'WbemScripting.SWbemNamedValueSet'; };
unless($@)
{
 $Context->Add("n1", [1, 2, 3]);
 $str = "The initial value of n1 is {";
 for ($x = 0; $x < @{$Context->Item("n1")->{Value}}; $x++)
 {
  $str = $str.@{$Context->Item("n1")->{Value}}[$x];
  if ($x != (@{$Context->Item("n1")->{Value}}) - 1 )
  {
   $str = $str.", ";
  }
 }
 $str = $str."}";
 print $str,"\n\n";

 # report the value of an element of the context value
 @v = @{$Context->Item("n1")->{Value}};
 print "By indirection the first element of n1 has value:", $v[0], "\n";

 # report the value directly
 print "By direct access the first element of n1 has value:", @{$Context->Item("n1")->{Value}}[0], "\n";

 # set the value of a single named value element
 @{$Context->Item("n1")->{Value}}[1] = 11;
 print "After direct assignment the first element of n1 has value:", 
       @{$Context->Item("n1")->{Value}}[1], "\n";

 # set the value of a single named value element
 @v = @{$Context->Item("n1")->{Value}};
 $v[1] = 345;
 print "After indirect assignment the first element of n1 has value:", 
    @{$Context->Item("n1")->{Value}}[1], "\n";

 # set the value of an entire context value
 $Context->Item("n1")->{Value} = [5, 34, 178871];
 print "After direct array assignment the first element of n1 has value:", 
   @{$Context->Item("n1")->{Value}}[1], "\n";

 $str = "After direct assignment the entire value of n1 is {";
 for ($x = 0; $x < @{$Context->Item("n1")->{Value}}; $x++)
 {
  $str = $str.@{$Context->Item("n1")->{Value}}[$x];
  if ($x != (@{$Context->Item("n1")->{Value}}) - 1 )
  {
   $str = $str.", ";
  }
 }
 $str = $str."}";
 print $str,"\n";
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMNAMEDVALUESET CLSID<br/>                                                    |
| IID<br/>                      | ISWbemNamedValueSet de IID \_<br/>                                                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de API de script](scripting-api-objects.md)
</dt> </dl>

 

 




