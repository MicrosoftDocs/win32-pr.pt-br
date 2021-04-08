---
title: Método INapClientManagement2 GetSystemIsolationInfoEx (NapManagement. h)
description: Recupera informações sobre o estado de isolamento e o estado de isolamento estendido do NapClient.
ms.assetid: 614bcf19-873e-4043-98b2-dcb152bae3e2
keywords:
- Método GetSystemIsolationInfoEx NAP
- Método GetSystemIsolationInfoEx NAP, interface INapClientManagement2
- INapClientManagement2 interface NAP, método GetSystemIsolationInfoEx
topic_type:
- apiref
api_name:
- INapClientManagement2.GetSystemIsolationInfoEx
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e75a6554ea7e55c3bebe35b797f888494a55627
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009166"
---
# <a name="inapclientmanagement2getsystemisolationinfoex-method"></a>Método INapClientManagement2:: GetSystemIsolationInfoEx

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **GetSystemIsolationInfoEx** recupera informações sobre o estado de isolamento e o estado de isolamento estendido do NapClient.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetSystemIsolationInfoEx(
  [out] IsolationInfoEx **isolationInfo,
  [out] BOOL            *unknownConnections
) const;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*isolationInfo* \[ fora\]
</dt> <dd>

Um ponteiro para um ponteiro para uma estrutura [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) que contém informações de estado de isolamento.

</dd> <dt>

*unknownConnections* \[ fora\]
</dt> <dd>

Um ponteiro para um BOOL que será **verdadeiro** se qualquer uma das conexões estiver em um estado desconhecido e **false** caso contrário.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um código de status HRESULT, incluindo, mas não se limitando a um dos itens a seguir.



| Código de retorno                                                                                         | Descrição                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                | Operação concluída com êxito.<br/>                                   |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>      | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>       | O limite de recursos do sistema não pôde executar a operação.<br/> |
| <dl> <dt>**RPC \_ E \_ desconectado**</dt> </dl> | O NapAgent não está em execução.<br/>                            |



 

## <a name="remarks"></a>Comentários

As informações de isolamento que são recuperadas não refletem Estados desconhecidos.

O SHA deve liberar a estrutura [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) chamando [**FreeIsolationInfoEx**](freeisolationinfoex.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                               |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                         |
| parâmetro<br/>                   | <dl> <dt>NapManagement. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapManagement. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>        |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapClientManagement2**](inapclientmanagement2.md)
</dt> </dl>

 

 





