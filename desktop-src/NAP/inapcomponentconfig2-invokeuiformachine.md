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
ms.openlocfilehash: 6bc0c09f802a63a5bfad92b49f76fcbb4ee242d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085493"
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

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK se for bem-sucedido ou um dos códigos de erro padrão do Windows.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapComponentConfig2**](inapcomponentconfig2.md)
</dt> </dl>

 

 





