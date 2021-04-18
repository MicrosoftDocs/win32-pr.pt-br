---
description: Recupera informações do sistema.
ms.assetid: 94C10DD6-FE49-4dd4-AEED-69B73A75EDEF
title: Método Shell. GetSystemInformation (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.GetSystemInformation
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 2ad7a865ba6ac5b62bc8a9b5ac105c0ef166d574
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968169"
---
# <a name="shellgetsysteminformation-method"></a>Método Shell. GetSystemInformation

Recupera informações do sistema.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = Shell.GetSystemInformation(
  sName
)
```


```VB

Shell.GetSystemInformation( _
  ByVal sName As BSTR _
) As Variant
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sname* \[ no\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Uma **cadeia de caracteres** que especifica as informações do sistema que estão sendo solicitadas.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

### <a name="jscript"></a>JScript

Tipo: **variante**

Retorna o valor das informações do sistema solicitadas. O tipo de retorno depende de quais informações do sistema são solicitadas. Consulte a seção comentários para obter detalhes.

### <a name="vb"></a>VB

Tipo: **variante**

Retorna o valor das informações do sistema solicitadas. O tipo de retorno depende de quais informações do sistema são solicitadas. Consulte a seção comentários para obter detalhes.

## <a name="remarks"></a>Comentários

Esse método pode ser usado para solicitar muitos valores de informações do sistema. A tabela a seguir fornece o valor de *sname* que é usado para solicitar as informações e o tipo associado do valor retornado.



*sName*

Tipo de retorno

Descrição

DirectoryServiceAvailable

**Booliano**

Defina como **true** se o serviço de diretório estiver disponível; caso contrário, **false**.

DoubleClicktime

**Inteiro**

O tempo de clique duplo, em milissegundos.

ProcessorLevel

**Inteiro**

**Windows Vista e posterior**. O nível do processador. Retorna 3, 4 ou 5, para os processadores de nível X386, x486 e Pentium, respectivamente.

ProcessorSpeed

**Inteiro**

A velocidade do processador, em megahertz (MHz).

ProcessorArchitecture

**Inteiro**

A arquitetura do processador. Para obter detalhes, consulte a discussão do membro **wProcessorArchitecture** da estrutura [**de \_ informações do sistema**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) .

PhysicalMemoryInstalled

**Inteiro**

A quantidade de memória física instalada, em bytes.

Os itens a seguir são válidos somente no Windows XP.

IsOS \_ Professional

**Booliano**

Defina como **true** se o sistema operacional for o Windows XP Professional Edition; caso contrário, **false**.

IsOS \_ pessoal

**Booliano**

Defina como **true** se o sistema operacional for o Windows XP Home Edition; caso contrário, **false**.

O seguinte é válido somente no Windows XP e posterior.

IsOS \_ DomainMember

**Booliano**

Defina como **true** se o computador for membro de um domínio; caso contrário, **false**.



 

Este método não está disponível atualmente no Microsoft Visual Basic.

## <a name="examples"></a>Exemplos

Os exemplos a seguir mostram o uso de **GetSystemInformation** para JScript e VBScript.

JScript


```JScript
<script language="JavaScript">
    function fnGetSystemInformationJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var vReturn;

        vReturn = objShell.GetSystemInformation("ProcessorLevel");
        document.write(vReturn);
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnGetSystemInformationVB()
        dim objShell
        dim vReturn

        set objShell = CreateObject("shell.application")

        vReturn = objShell.GetSystemInformation("ProcessorLevel")
        document.write(vReturn)

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| INSERI<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5,0 ou posterior)</dt> </dl> |



 

 
