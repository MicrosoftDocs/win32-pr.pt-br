---
title: Método INapComponentConfig2 InvokeUIForMachine (NapCommon. h)
description: É implementado por SHVs (validadores da integridade do sistema) conforme necessário para gerenciar a configuração remota diretamente no computador especificado. Esse método inicia uma interface do usuário de gerenciamento de configuração.
ms.assetid: 67a6d715-250b-4b8b-9c27-8173926b7bfe
keywords:
- Método InvokeUIForMachine NAP
- Método InvokeUIForMachine NAP, interface INapComponentConfig2
- INapComponentConfig2 interface NAP, método InvokeUIForMachine
topic_type:
- apiref
api_name:
- INapComponentConfig2.InvokeUIForMachine
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8321425cf878bd9b3d8702f73fa464ae069420cd0e59f57e2500151fda01b191
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940184"
---
# <a name="inapcomponentconfig2invokeuiformachine-method"></a>Método INapComponentConfig2:: InvokeUIForMachine

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **InvokeUIForMachine** é implementado por SHVs (validadores da integridade do sistema) conforme necessário para gerenciar a configuração remota diretamente no computador especificado. Esse método inicia uma interface do usuário de gerenciamento de configuração.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT InvokeUIForMachine(
  [in] HWND          hwndParent,
  [in] CountedString *machineName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hwndParent* \[ no\]
</dt> <dd>

Um identificador para a janela pai ou proprietário. Um identificador de janela válido deve ser fornecido.

</dd> <dt>

*MachineName* \[ no\]
</dt> <dd>

Um ponteiro para um [**contadostring**](/windows/win32/api/naptypes/ns-naptypes-countedstring) que contém o nome do computador do cliente NAP.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

retorna S \_ OK se for bem-sucedido ou um dos Windows códigos de erro padrão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                     |
| Cabeçalho<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapComponentConfig2**](inapcomponentconfig2.md)
</dt> </dl>

 

 





