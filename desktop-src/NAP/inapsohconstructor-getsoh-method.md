---
title: Método GetSoHConstructor INapSoH (NapProtocol.h)
description: Recupera o pacote SoHRequest ou SoHResponse construído.
ms.assetid: 402c72fd-9e23-453a-8c95-57615295e056
keywords:
- NAP do método GetSoH
- Método GetSoH NAP, interface INapSoHConstructor
- Interface INapSoHConstructor NAP, método GetSoH
topic_type:
- apiref
api_name:
- INapSoHConstructor.GetSoH
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3d411d57ae77a1e5bf8c04ca0d9d980a9c33e9fcf15eb05f157ddeda98711c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118133819"
---
# <a name="inapsohconstructorgetsoh-method"></a>Método INapSoHConstructor::GetSoH

> [!Note]  
> A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10

 

O **método INapSoHConstructor::GetSoH** recupera o pacote SoHRequest ou SoHResponse construído.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetSoH(
  [out] SoH **soh
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*soh* \[ out\]
</dt> <dd>

Um ponteiro para um ponteiro para o pacote [**SoHRequest ou**](/windows/win32/api/naptypes/ns-naptypes-soh) **SoHResponse** construído.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Outros códigos de erro específicos do COM também podem ser retornados.



| Código de retorno                                                                                     | Descrição                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Operação concluída com êxito.<br/>                                   |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite de recursos do sistema, não foi possível executar a operação.<br/> |



 

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

 

 





