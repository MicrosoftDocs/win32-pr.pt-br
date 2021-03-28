---
description: Notificação enviada ao objeto de retorno de chamada de exibição para especificar os locais e eventos que devem ser registrados para eventos de notificação de alteração.
title: Mensagem de SFVM_GETNOTIFY (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 87933217-dfa9-4aaf-9630-fa2c302b18fa
api_name:
- SFVM_GETNOTIFY
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f766ee74463dd820c0b55d501d5002a3378a97b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170320"
---
# <a name="sfvm_getnotify-message"></a>Mensagem de SFVM \_ GETnotify

Notificação enviada ao objeto de retorno de chamada de exibição para especificar os locais e eventos que devem ser registrados para eventos de notificação de alteração. Depois que eles são registrados, quando uma alteração ocorre no nesses locais ou eventos, o objeto exibir retorno de chamada é notificado. Esses eventos são enviados para o retorno de chamada de exibição por meio de [**SFVM \_ FSNOTIFY**](sfvm-fsnotify.md) e, em seguida, são tratados pelo modo de exibição.


```C++
SFVM_GETNOTIFY 

    wParam = (WPARAM)(LPITEMIDLIST*) pidl;

    lParam = (LPARAM)(LONG*) lEvents;

            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PIDL* \[ fora\]
</dt> <dd>

Um ponteiro para um IDList absoluto de um item para o qual a exibição deve se registrar para ser notificado das alterações. Normalmente, isso é o mesmo que o IDList do local que está sendo exibido, mas pode ser outro local.

> [!IMPORTANT]
> O tempo de vida desse valor é de Propriedade do objeto de retorno de chamada de exibição. É responsabilidade do objeto exibir retorno de chamada criar e, em seguida, liberar esse valor quando ele não for mais necessário. Isso requer que o objeto de retorno de chamada de exibição armazene esse valor. Normalmente, o valor pode ser armazenado no membro **\_ pidlMonitor** do objeto View callback. As regras de propriedade para o valor retornado por meio de *PIDL* não são padrão e exigem cuidados especiais. O objeto de retorno de chamada de exibição deve possuir esse valor e garantir que ele não seja liberado até que o objeto de retorno de chamada de exibição seja destruído.

 

</dd> <dt>

*lEvents* \[ fora\]
</dt> <dd>

Um valor que contém um ou mais valores SHCNE. Consulte [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) para obter uma lista de possíveis valores. O objeto exibir retorno de chamada será registrado para receber uma mensagem [**SFVM \_ FSNOTIFY**](sfvm-fsnotify.md) quando qualquer um dos eventos associados ocorrer.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Ignorado, mas deve retornar S \_ OK.

## <a name="remarks"></a>Comentários

Se essa mensagem de retorno de chamada não retornar um valor diferente de zero para o IDList ou a máscara de eventos, a exibição não será registrada para notificações de alteração.

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra uma implementação de exemplo do código do manipulador da função de retorno de chamada para **SFVM \_ getnotificate**.


```C++
case SFVM_GETNOTIFY:
  *((LPITEMIDLIST*)wParam) = _pidl;    // Pass a reference whose lifetime this 
                                       // class is responsible for.
                                      
  *((LONG*)lParam) = SHCNE_DISKEVENTS; // A combination of all of the 
                                       // disk event identifiers.
                                       
   return S_OK;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SFVM \_ QUERYFSNOTIFY**](sfvm-queryfsnotify.md)
</dt> <dt>

[**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)
</dt> </dl>

 

 
