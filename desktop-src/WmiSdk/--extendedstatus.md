---
description: Usado para relatar informações detalhadas sobre o status e o erro.
ms.assetid: 6bdff9a8-1a7c-4860-a12e-4d3162964ee4
ms.tgt_platform: multiple
title: Classe __ExtendedStatus
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ExtendedStatus
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: cfc364ac6523aad69e53755d96fe220d0109fab8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105787639"
---
# <a name="__extendedstatus-class"></a>\_\_Classe ExtendedStatus

A classe de sistema **\_ \_ ExtendedStatus** é usada para relatar informações detalhadas de status e erro.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class __ExtendedStatus : __NotifyStatus
{
  string Description;
  string Operation;
  string ParameterInfo;
  string ProviderName;
  uint32 StatusCode;
};
```

## <a name="members"></a>Membros

A classe **\_ \_ ExtendedStatus** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **\_ \_ ExtendedStatus** tem essas propriedades.

<dl> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Qualquer cadeia de caracteres definida pelo usuário que descreva um erro ou status operacional.

</dd> <dt>

**Operação**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Operação que ocorre no momento de uma falha ou anomalia. Normalmente, Instrumentação de Gerenciamento do Windows (WMI) define essa propriedade como o nome de uma API COM para o método WMI, como o seguinte: [**IWbemServices:: CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum).

</dd> <dt>

**ParameterInfo**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Parâmetros envolvidos em um erro ou alteração de status. Por exemplo, se um aplicativo tentar recuperar uma classe que não existe, essa propriedade será definida como o nome da classe incorreta.

</dd> <dt>

**ProviderName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Identifica o provedor que causa ou relata um erro ou uma alteração de status. Se um provedor não estiver envolvido, essa cadeia de caracteres será definida como "Gerenciamento do Windows".

</dd> <dt>

**StatusCode**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Contém um código de erro ou informações para uma operação. Pode ser qualquer valor definido pelo provedor, mas o valor 0 (zero) geralmente é reservado para indicar êxito. Essa propriedade é herdada de [**\_ \_ NotifyStatus**](--notifystatus.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **\_ \_ ExtendedStatus** é derivada da classe [**\_ \_ NotifyStatus**](--notifystatus.md) .

Use a classe **\_ \_ ExtendedStatus** para relatar informações mais complexas do que um código de resultado simples. Os provedores podem derivar suas próprias classes de **\_ \_ ExtendedStatus** se exigirem mais propriedades para descrever os erros.

A propriedade **StatusCode** , herdada da classe pai [**\_ \_ NotifyStatus**](--notifystatus.md) , é um inteiro sem sinal que representa o erro ou o valor de status. Quando as instâncias dessa classe são retornadas de um método por um provedor dinâmico, as propriedades **StatusCode** e **Description** são definidas pelo provedor e as outras propriedades são definidas pelo WMI.

## <a name="examples"></a>Exemplos

O exemplo de código a seguir, extraído do [FND: como tratar Configuration Manager erros assíncronos usando](https://Gallery.TechNet.Microsoft.Com/0bc05d07-1479-43c9-8e01-0f01d0fc3daa) o exemplo de código do WMI VBScript na galeria do TechNet, descreve como usar o **\_ \_ ExtendedStatus** para recuperar informações de erro.


```VB
Sub sink_OnCompleted(HResult, oErr, oCtx) 
    WScript.Echo "All collections returned" 
  
    if HResult <> 0 Then  
    ' Determine the type of error. 
        If oErr.Path_.Class = "__ExtendedStatus" Then 
            WScript.Echo "WMI Error: "& oErr.Description             
        ElseIf ExtendedStatus.Path_.Class = "SMS_ExtendedStatus" Then 
            WScript.Echo "Provider Error: "& oErr.Description 
            WScript.Echo "Code: " & oErr.ErrorCode 
        End If 
    End If     
    bdone = true 
End sub
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Todos os namespaces do WMI<br/>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_\_NotifyStatus**](/windows/desktop/WmiSdk/--notifystatus)
</dt> <dt>

[Classes do sistema WMI](wmi-system-classes.md)
</dt> </dl>

 

