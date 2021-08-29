---
title: Método INapSoHConstructor Initialize (NapProtocol.h)
description: Inicializa um pacote de protocolo SoH no sistema NAP.
ms.assetid: 1678b677-c8c8-465c-a412-9b929e39bbac
keywords:
- Inicializar o método NAP
- Inicializar o método NAP, interface INapSoHConstructor
- INapSoHConstructor interface NAP , método Initialize
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
ms.openlocfilehash: 3d03d821b441aa71f4766fc255f48122fe4f2c432d60d52ab957022d7be50a79
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803026"
---
# <a name="inapsohconstructorinitialize-method"></a>Método INapSoHConstructor::Initialize

> [!Note]  
> A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10

 

O **método INapSoHConstructor::Initialize** inicializa um pacote de protocolo SoH no sistema NAP.

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

Um [SystemHealthEntityId exclusivo](nap-datatypes.md) que contém a ID do SHA ou SHV que está construindo o pacote.

</dd> <dt>

*isRequest* \[ Em\]
</dt> <dd>

Um **BOOL** que será **TRUE** se o pacote for [**um SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) e **FALSE** se for um **SoHResponse**.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Outros códigos de erro específicos do COM também podem ser retornados.



| Código de retorno                                                                                     | Descrição                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Operação concluída com êxito.<br/>                                   |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite de recursos do sistema, não foi possível executar a operação.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método deve ser chamado exatamente uma vez por pacote.

O [SystemHealthEntityId](nap-datatypes.md) especificado em *id* é o primeiro TLV no pacote SOH recém-construído e tem o tipo de atributo [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                       |
| Cabeçalho<br/>                   | <dl> <dt>NapProtocol.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapProtocol.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapSoHConstructor**](inapsohconstructor.md)
</dt> </dl>

 

 





