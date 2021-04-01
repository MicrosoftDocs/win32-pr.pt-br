---
description: O especialista implementa a função DllMain. O sistema operacional chama DllMain para obter um identificador para uma instância do especialista.
ms.assetid: 38593ba0-dc37-4620-bb49-2e50c3d9ea3c
title: Função de retorno de chamada de especialista de DllMain (Process. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DllMain
api_type:
- UserDefined
api_location:
- process.h
ms.openlocfilehash: 914f50b75e83fdc67448770b32ac8d0f8e8ab656
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828965"
---
# <a name="dllmain-expert-callback-function"></a>Função de retorno de chamada de especialista de DllMain

O especialista implementa a função [**DllMain**](/windows/desktop/Dlls/dllmain) . O sistema operacional chama **DllMain** para obter um identificador para uma instância do especialista.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI DllMain(
  _Out_ HINSTANCE hInstance,
  _In_  ULONG     ulReason,
        LPVOID    Reserved
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HINSTANCE* \[ fora\]
</dt> <dd>

Manipule a uma instância do especialista.

Se o especialista usar a interface do usuário Monitor de Rede, o valor *HINSTANCE* deverá ser armazenado em uma variável global. Essa abordagem é necessária somente quando o valor do parâmetro *ulReason* é definido como dll de \_ processo \_ Attach.

</dd> <dt>

*ulReason* \[ no\]
</dt> <dd>

Indicador de por que a função foi chamada. Um valor de \_ anexação do processo de dll \_ , (que se aplica quando a dll é carregada pela primeira vez) indica que o especialista deve salvar o valor *HINSTANCE* em uma variável global.

Com qualquer outro valor, todas as chamadas para a função [**DllMain**](/windows/desktop/Dlls/dllmain) podem ser ignoradas. Para obter uma lista de todos os sinalizadores possíveis definidos pelo sistema operacional, consulte **DllMain**.

</dd> <dt>

*Reserved* 
</dt> <dd>

O parâmetro não está em uso.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será **true**.

Se a função não for bem-sucedida, o valor de retorno será **false**.

## <a name="remarks"></a>Comentários

O sistema operacional chama a função de especialista de **DllMain** quando um processo carrega ou descarrega a DLL de especialista. A função de especialista de **DllMain** deve ser exportada somente se o especialista tiver uma interface do usuário para exibir a configuração ou os resultados e, em seguida, apenas para retornar o valor apropriado de *HINSTANCE* .

A função de especialista de **DllMain** é baseada na função [**DllMain**](/windows/desktop/Dlls/dllmain) da biblioteca de vínculo dinâmico.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Process. h</dt> </dl> |



 

