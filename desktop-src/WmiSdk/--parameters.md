---
description: Define os parâmetros de entrada e saída para métodos.
ms.assetid: d973feb5-27c4-4d8e-bf1b-0a455afa4375
ms.tgt_platform: multiple
title: Classe __PARAMETERS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __PARAMETERS
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: a2f39cb7b88977c8f61e562badaa6cbda7a5004fc2d0edf70eb59c6276070efd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118110561"
---
# <a name="__parameters-class"></a>\_\_Classe Parameters

A classe de sistema **\_ \_ Parameters** é uma classe abstrata que define os parâmetros de entrada e saída para métodos. Ele também é usado para passar valores de parâmetros de entrada e saída entre um cliente WMI e um provedor de métodos.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[abstract]
class __PARAMETERS
{
};
```

## <a name="members"></a>Membros

A classe **\_ \_ Parameters** não define nenhum membro.

## <a name="remarks"></a>Comentários

Para definir um método em uma classe de usuário, um cliente WMI cria uma cópia da classe **\_ \_ Parameters** e adiciona uma propriedade para cada parâmetro de entrada em um método. Se o método contiver um valor de retorno ou parâmetros de saída, outra cópia dos **\_ \_ parâmetros** deverá ser criada. Se o método retornar um valor de retorno, o cliente deverá adicionar uma propriedade chamada **ReturnValue**. O provedor de método, em seguida, armazena os parâmetros do método com uma chamada para [**IWbemClassObject::P utmethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).

Para invocar um método, um cliente chama o seguinte em sequência:

1.  [**IWbemClassObject:: GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) para recuperar uma cópia da classe **\_ \_ Parameters** que é armazenada por [**IWbemClassObject::P utmethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).
2.  [**IWbemClassObject:: SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance)e, em seguida, define uma propriedade para cada parâmetro de entrada para o método.
3.  [**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) ou [**IWbemServices:: ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) para executar o método.

Depois que o método terminar a execução, outra instância de classe de **\_ \_ parâmetros** poderá ser retornada se o método tiver parâmetros de saída ou um valor de retorno.

-   Se o método foi invocado usando [**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod), a instância de **\_ \_ parâmetros** é retornada como um argumento de saída.
-   Se o método foi invocado usando [**IWbemServices:: ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync), a instância de **\_ \_ parâmetros** será retornada como um parâmetro para [**IWbemObjectSink:: indica**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Todos os namespaces do WMI<br/>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Classes do sistema WMI](wmi-system-classes.md)
</dt> <dt>

[**IWbemServices:: ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)
</dt> <dt>

[Chamando um método](calling-a-method.md)
</dt> </dl>

 

 




