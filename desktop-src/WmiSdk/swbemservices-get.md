---
description: Recupera um objeto , que é uma definição de classe ou uma instância, com base no caminho do objeto.
ms.assetid: 3071aeb2-adab-47aa-a10c-9796766bb630
ms.tgt_platform: multiple
title: Método SWbemServices.Get (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.Get
- ISWbemServices.Get
- ISWbemServices.Get
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d448d92cddf24e98f05cf023116e7087ad8cc3dcd310b7ccd3657571ee7650ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118312655"
---
# <a name="swbemservicesget-method"></a>Método SWbemServices.Get

O **método Get** do objeto [**SWbemServices**](swbemservices.md) recupera um objeto , que é uma definição de classe ou uma instância, com base no caminho do objeto. Esse método recupera apenas objetos do namespace associado ao objeto **SWbemServices** atual.

O método é chamado no modo síncrono. Para obter mais informações, consulte [Chamando um método](calling-a-method.md).

Para uma explicação dessa sintaxe, consulte [Convenções de documento para a API de Script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
objWbemObject = .Get( _
  [ ByVal strObjectPath ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*strObjectPath* \[ Opcional\]
</dt> <dd>

Cadeia de caracteres que contém o caminho do objeto a ser recuperado. Se esse valor estiver vazio, o objeto vazio retornado poderá se tornar uma nova classe. Para obter mais informações, [consulte Descrevendo o local de um objeto WMI](describing-the-location-of-a-wmi-object.md).

</dd> <dt>

*iFlags* \[ Opcional\]
</dt> <dd>

Inteiro que determina o comportamento da consulta. Esse parâmetro pode aceitar os valores a seguir.

<dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers*** (131072 (0x20000))


</dt> <dd>

Faz com que o WMI retorne dados de alteração de classe com a definição de classe base. Para obter mais informações sobre qualificadores corrigidos, consulte [Localizando informações de classe WMI](localizing-wmi-class-information.md).

</dd> </dl> </dd> <dt>

*objWbemNamedValueSet* \[ Opcional\]
</dt> <dd>

Normalmente, isso é indefinido. Caso contrário, esse é [**um objeto SWbemNamedValueSet**](swbemnamedvalueset.md) cujos elementos representam as informações de contexto que podem ser usadas pelo provedor que está atendendo à solicitação. Um provedor que dá suporte ou requer essas informações deve documentar os nomes de valor reconhecidos, o tipo de dados do valor, os valores permitidos e a semântica.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se for bem-sucedido, esse método retornará [**um objeto SWbemObject**](swbemobject.md) que representa o objeto solicitado.

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do método **Get,** o **objeto Err** pode conter um dos códigos de erro na lista a seguir.

<dl> <dt>

**wbemErrAccessDenied** – 2147749891 (0x80041003)
</dt> <dd>

O usuário atual não tem a permissão para acessar o objeto .

</dd> <dt>

**wbemErrFailed** – 2147749889 (0x80041001)
</dt> <dd>

Erro não especificado.

</dd> <dt>

**wbemErrInvalidParameter** – 2147749896 (0x80041008)
</dt> <dd>

Um parâmetro especificado não é válido.

</dd> <dt>

**wbemErrInvalidObjectPath** – 2147749946 (0x8004103A)
</dt> <dd>

O caminho especificado não era válido.

</dd> <dt>

**wbemErrNotFound** – 2147749890 (0x80041002)
</dt> <dd>

Não foi possível encontrar o objeto solicitado.

</dd> <dt>

**wbemErrOutOfMemory** – 2147749894 (0x80041006)
</dt> <dd>

Não há memória suficiente para concluir a operação.

</dd> </dl>

## <a name="remarks"></a>Comentários

Ao contrário [**dos métodos ExecQuery**](/windows/desktop/api/Provider/nf-provider-provider-execquery) e [**InstancesOf,**](swbemservices-instancesof.md) o método Get sempre retorna um [**SWbemObject que**](swbemobject.md) representa uma instância específica de um recurso gerenciado por WMI. Para obter uma instância específica de um recurso gerenciado por WMI usando o método Get, você deve dizer para Obter a instância a ser recuperada passando o caminho do objeto ao método , conforme mostrado no script a seguir.


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set objSWbemObject = objSWbemServices.Get("Win32_Service.Name='Messenger'")
Wscript.Echo "Name:         " & objSWbemObject.Name        & vbCrLf & _
             "Display Name: " & objSWbemObject.DisplayName & vbCrLf & _
             "Start Mode:   " & objSWbemObject.StartMode   & vbCrLf & _
             "State:        " & objSWbemObject.State
```



Você pode usar esse método para obter [*objetos singleton,*](gloss-s.md) como [**\_ \_ CIMOMIdentification**](--cimomidentification.md), que contém informações de versão sobre a instalação do WMI em execução.

Você pode examinar o repositório com uma ferramenta de exibição, como [o CIM Studio,](further-information.md) para verificar se a nova classe e a instância aparecem. Para ver um exemplo de como remover uma classe e uma instância do repositório, consulte [**SWbemServices.Delete**](swbemservices-delete.md) ou [**SWbemObject.Delete. \_**](swbemobject-delete-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemServices<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemServices<br/>                                                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SWbemServices**](swbemservices.md)
</dt> <dt>

[**Swbemobject**](swbemobject.md)
</dt> </dl>

 

 




