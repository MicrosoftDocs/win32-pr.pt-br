---
description: Retorna uma representação XML de um objeto ou instância. O arquivo de texto é formatado no formato XML especificado, conforme mostrado em WbemObjectTextFormatEnum.
ms.assetid: 98961d94-8360-4ed7-b1b1-20b4fca45d45
ms.tgt_platform: multiple
title: SWbemObjectEx.GetText_ método (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectEx.GetText_
- ISWbemObjectEx.GetText_
- ISWbemObjectEx.GetText_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a75adbab65c735a298c6a1599718cc6df5b690dd
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122623322"
---
# <a name="swbemobjectexgettext_-method"></a>Método SWbemObjectEx.GetText \_

O **método \_ GetText** do objeto [**SWbemObjectEx**](swbemobjectex.md) retorna uma representação XML de um objeto ou instância. O arquivo de texto é formatado no formato XML especificado, conforme mostrado em [**WbemObjectTextFormatEnum.**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum)

Para uma explicação dessa sintaxe, consulte [Convenções de documento para a API de Script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
strObj = .GetText_( _
  ByVal iTextFormat, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*iTextFormat* \[ Em\]
</dt> <dd>

Obrigatórios. Um valor de [**WbemObjectTextFormatEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum) que especifica o formato XML resultante.

</dd> <dt>

*iFlags* \[ in, opcional\]
</dt> <dd>

Sinalizadores de operação reservada. O valor padrão é 0 (zero).

</dd> <dt>

*objWbemNamedValueSet* \[ in, opcional\]
</dt> <dd>

Um [**objeto SWbemNamedValueSet**](swbemnamedvalueset.md) que define o contexto para a operação. O padrão é nulo. Para obter mais informações sobre os pares de nome/valor permitidos, consulte Comentários abaixo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não tem valores de retorno.

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do **método \_ GetText,** o **objeto Err** pode conter um dos códigos de erro na lista a seguir.

<dl> <dt>

**wbemErrFailed** – 2147749889 (0x80041001)
</dt> <dd>

Erro não especificado.

</dd> <dt>

**wbemErrNotFound** – 2147749890 (0x80041002)
</dt> <dd>

O formato solicitado não foi encontrado.

</dd> <dt>

**wbemErrInvalidParameter** – 2147749896 (0x80041008)
</dt> <dd>

Um dos parâmetros para a chamada não está correto.

</dd> <dt>

**wbemErrCriticalError** – 2147749898 (0x8004100A)
</dt> <dd>

Ocorreu um erro interno, crítico e inesperado. Relate este erro ao Suporte Técnico da Microsoft.

</dd> </dl>

## <a name="remarks"></a>Comentários

Ao construir seu [**SWbemNamedValueSet**](swbemnamedvalueset.md), somente os pares de nome/valor a seguir são permitidos.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Nome</th>
<th>Valor</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Localonly</td>
<td><strong>VT_BOOL</strong><br/> Se <strong>TRUE</strong>, somente as propriedades e os métodos definidos localmente estão presentes no XML resultante. O padrão é <strong>FALSE.</strong><br/></td>
</tr>
<tr class="even">
<td>IncludeQualifiers</td>
<td><strong>VT_BOOL</strong><br/> Se <strong>TRUE</strong>, os qualificadores de classes, instâncias, propriedades e métodos serão incluídos no XML resultante. O padrão é <strong>FALSE.</strong><br/></td>
</tr>
<tr class="odd">
<td>PathLevel</td>
<td><strong>VT-I4</strong><br/> O padrão é 0 (zero). Os valores possíveis são:<br/>
<ul>
<li>0: um <CLASS> elemento ou é criado <INSTANCE> dependendo se o objeto é uma classe ou instância.</li>
<li>1: um <VALUE.NAMEDOBJECT> elemento é gerado.</li>
<li>2: um <VALUE.OBJECTWITHLOCALPATH> elemento é gerado.</li>
<li>3: um <VALUE.OBJECTWITHPATH> elemento é gerado.</li>
</ul></td>
</tr>
<tr class="even">
<td>ExcludeSystemProperties</td>
<td><strong>VT-BOOL</strong><br/> Se <strong>TRUE</strong>, as propriedades do sistema, como __NAMESPACE, serão excluídas da saída.<br/></td>
</tr>
<tr class="odd">
<td>IncludeClassOrigin</td>
<td><strong>VT_BOOL</strong><br/> Se <strong>TRUE</strong>, o atributo de origem da classe será definido nos <PROPERTY> elementos e <METHOD> . O padrão é <strong>FALSE.</strong><br/></td>
</tr>
</tbody>
</table>



 

Para obter mais informações sobre como [**criar um SWbemNamedValueSet**](swbemnamedvalueset.md), consulte [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md).

## <a name="examples"></a>Exemplos

O script a seguir mostra como obter uma representação XML da definição da [**classe Win32 \_ Bios.**](/windows/desktop/CIMWin32Prov/win32-bios) Especificando uma instância específica do **Win32 \_ Bios,** você pode obter os dados desse objeto em XML.


```VB
' Connect to the default namespace (root\cimv2) with the default
' impersonation level ("impersonate") and obtain a Win32_Bios class
' object.
Set obj = GetObject("winmgmts:win32_bios")

' Use the value for the desired XML CIM DTD format. 
XMLDtd = 1
Text = obj.GetText_(XMLDtd)
wscript.echo Text
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObjectEx<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemObjectEx<br/>                                                          |



 

