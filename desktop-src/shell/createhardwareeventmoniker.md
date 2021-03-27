---
description: Cria um moniker que representa um componente de hardware e seu manipulador de eventos associado. A reprodução automática usa essa função para permitir que os aplicativos usem eventos de reprodução automática.
title: Função CreateHardwareEventMoniker
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateHardwareEventMoniker
api_type:
- DllExport
api_location:
- Shsvcs.dll
ms.assetid: ff0ad023-42ea-4c74-adae-af55527b6ac3
ms.openlocfilehash: 59100ab20cd997cc4ab35602698268ec6d76dea4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967346"
---
# <a name="createhardwareeventmoniker-function"></a>Função CreateHardwareEventMoniker

\[Essa função está disponível por meio do Windows XP com Service Pack 2 (SP2) e Windows Server 2003. Ele pode ser alterado ou indisponível nas versões subsequentes do Windows.\]

Cria um moniker que representa um componente de hardware e seu manipulador de eventos associado. A reprodução automática usa essa função para permitir que os aplicativos usem eventos de reprodução automática.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CreateHardwareEventMoniker(
  _In_  REFCLSID clsid,
  _In_  LPCTSTR  pszEventHandler,
  _Out_ IMoniker **ppmoniker
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*CLSID* \[ do no\]
</dt> <dd>

Tipo: **REFCLSID**

A ID da classe à qual o moniker é associado.

</dd> <dt>

*pszEventHandler* \[ no\]
</dt> <dd>

Tipo: **LPCTSTR**

O nome do manipulador de eventos.

</dd> <dt>

*ppmoniker* \[ fora\]
</dt> <dd>

Tipo: **[ **IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker)\*\***

O endereço de uma variável de ponteiro que recebe o ponteiro de interface [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se essa função for bem sucedido, ela retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Use **CreateHardwareEventMoniker** ao registrar aplicativos em execução para que esses aplicativos tenham acesso aos eventos de reprodução automática. Para usar eventos de reprodução automática em aplicativos em execução, você deve primeiro criar um novo componente que implementa a interface [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) . Inicialize essa interface com o valor InitCmdLine da entrada do manipulador em particular sob a chave de **manipuladores** , porque a reprodução automática não chama o método [**Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ihweventhandler-initialize) .

Você deve chamar **CreateHardwareEventMoniker** para obter um moniker que represente seu componente e seu manipulador de eventos. Em seguida, use o valor retornado no parâmetro *ppmoniker* para registrar seu componente na tabela de objetos em execução (corrompidos), conforme mostrado no exemplo.

Observe que **CreateHardwareEventMoniker** não está definido em um arquivo de cabeçalho. Para usá-lo em seu código, você deve obter um identificador para o arquivo de Shsvcs.dll por meio de uma chamada para [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya). Em seguida, você usa esse identificador em uma chamada para [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para obter uma instância da função **CreateHardwareEventMoniker** .

A chamada para [**IRunningObjectTable:: Register**](/windows/win32/api/objidl/nf-objidl-irunningobjecttable-register) exige que você insira as seguintes informações de **AppID** no registro.

```
HKEY_CLASSES_ROOT
   AppID
      MyApp.exe
         (Default) = MyApplication
         AppID [REG_SZ] = {Your GUID here}
```

```
HKEY_CLASSES_ROOT
   AppID
      {The same GUID here}
         (Default) = MyApplication
         RunAs = Interactive User
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Nenhum</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Shsvcs.dll</dt> </dl> |



 

 
