---
title: Método de validação de INapSoHConstructor (NapProtocol. h)
description: Verifica a validade do pacote SoH.
ms.assetid: 66338213-43c0-461a-a794-5f18d56bd505
keywords:
- Validar método NAP
- Validar método NAP, interface INapSoHConstructor
- INapSoHConstructor interface NAP, método Validate
topic_type:
- apiref
api_name:
- INapSoHConstructor.Validate
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7db8a52d7986348e85c724171b6d417996c7315
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644926"
---
# <a name="inapsohconstructorvalidate-method"></a>Método INapSoHConstructor:: Validate

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **INapSoHConstructor:: Validate** verifica a validade do pacote soh.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Validate(
  [in] const SoH  *soh,
  [in]       BOOL isRequest
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*soh* \[ no\]
</dt> <dd>

Um ponteiro para o pacote [**soh**](/windows/win32/api/naptypes/ns-naptypes-soh) construído.

</dd> <dt>

*Isrequest* \[ no\]
</dt> <dd>

Um **bool** que será **verdadeiro** se o pacote for um [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) e **false** se for um **SoHResponse**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Outros códigos de erro específicos de COM também podem ser retornados.



| Código de retorno                                                                                            | Descrição                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | O pacote SoH é válido.<br/>                                |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>        | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>         | O limite de recursos do sistema não pôde executar a operação.<br/> |
| <dl> <dt>**\_pacote NAP E \_ inválido \_**</dt> </dl> | O pacote SoH é inválido.<br/>                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                       |
| parâmetro<br/>                   | <dl> <dt>NapProtocol. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapProtocol. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl>       |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**INapSoHConstructor**](inapsohconstructor.md)
</dt> </dl>

 

 





