---
title: Método INapComponentConfig InvokeUI (NapCommon. h)
description: Inicia uma interface do usuário personalizada para um componente do validador da integridade do sistema (SHV).
ms.assetid: da2a5e3e-bc17-4984-bdbe-b72e9e710a9d
keywords:
- Método InvokeUI NAP
- Método InvokeUI NAP, interface INapComponentConfig
- INapComponentConfig interface NAP, método InvokeUI
topic_type:
- apiref
api_name:
- INapComponentConfig.InvokeUI
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dd86d683365286fc2130c1ac9edf21ff075d61a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918245"
---
# <a name="inapcomponentconfiginvokeui-method"></a>Método INapComponentConfig:: InvokeUI

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **InvokeUI** inicia uma interface do usuário personalizada para um componente do validador da integridade do sistema (SHV).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT InvokeUI(
  [in] HWND hwndParent
) const;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hwndParent* \[ no\]
</dt> <dd>

Um identificador para a janela pai ou proprietário. Um identificador de janela válido deve ser fornecido.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos seguintes códigos de erro com base no resultado dessa operação.



| Código de retorno                                                                                     | Descrição                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | A operação teve êxito.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | O limite de recursos do sistema não pôde executar a operação.<br/> |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>       | O SHV não oferece suporte a uma interface do usuário personalizada.<br/>               |



 

## <a name="remarks"></a>Comentários

Essa chamada de método deve ser bloqueada até que a interface do usuário do SHV saia.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapComponentConfig**](inapcomponentconfig.md)
</dt> <dt>

[**INapComponentConfig::IsUISupported**](inapcomponentconfig-isuisupported.md)
</dt> </dl>

 

 





