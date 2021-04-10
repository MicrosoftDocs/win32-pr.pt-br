---
title: Método de inicialização de INapSoHConstructor (NapProtocol. h)
description: Inicializa um pacote de protocolo SoH no sistema NAP.
ms.assetid: 1678b677-c8c8-465c-a412-9b929e39bbac
keywords:
- Inicializar método NAP
- Método Initialize NAP, interface INapSoHConstructor
- INapSoHConstructor interface NAP, método Initialize
topic_type:
- apiref
api_name:
- INapSoHConstructor.Initialize
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eab8d6b27547be6e7c7e9abb59f7edb7b49e716e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918376"
---
# <a name="inapsohconstructorinitialize-method"></a>Método INapSoHConstructor:: Initialize

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **INapSoHConstructor:: Initialize** Inicializa um pacote de protocolo soh no sistema NAP.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Initialize(
  [in] SystemHealthEntityId id,
  [in] BOOL                 isRequest
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ID* \[ em\]
</dt> <dd>

Um [SystemHealthEntityId](nap-datatypes.md) exclusivo que contém a ID do SHA ou SHV que está construindo o pacote.

</dd> <dt>

*Isrequest* \[ no\]
</dt> <dd>

Um **bool** que será **verdadeiro** se o pacote for um [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) e **false** se for um **SoHResponse**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Outros códigos de erro específicos de COM também podem ser retornados.



| Código de retorno                                                                                     | Descrição                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Operação concluída com êxito.<br/>                                   |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | O limite de recursos do sistema não pôde executar a operação.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método deve ser chamado exatamente uma vez por pacote.

O [SystemHealthEntityId](nap-datatypes.md) especificado na *ID* é o primeiro TLV no pacote soh criado recentemente e tem o tipo de atributo [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                       |
| parâmetro<br/>                   | <dl> <dt>NapProtocol. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapProtocol. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapSoHConstructor**](inapsohconstructor.md)
</dt> </dl>

 

 





