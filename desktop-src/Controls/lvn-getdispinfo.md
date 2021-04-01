---
title: LVN_GETDISPINFO código de notificação (commctrl. h)
description: Enviado por um controle de exibição de lista para sua janela pai. É uma solicitação para que a janela pai forneça as informações necessárias para exibir ou classificar um item de exibição de lista. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 04310e39-69bc-45d7-958c-00452279d7a9
keywords:
- LVN_GETDISPINFO de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- LVN_GETDISPINFO
- LVN_GETDISPINFOA
- LVN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1585524dd447c4a1324dc5c7a235490de776fb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645275"
---
# <a name="lvn_getdispinfo-notification-code"></a>Código de notificação do LVN \_ GETDISPINFO

Enviado por um controle de exibição de lista para sua janela pai. É uma solicitação para que a janela pai forneça as informações necessárias para exibir ou classificar um item de exibição de lista. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
LVN_GETDISPINFO
        
    pdi = (NMLVDISPINFO*) lParam
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) . Na entrada, a estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) contida nessa estrutura especifica o tipo de informação necessário e identifica o item ou subitem de interesse. Use a estrutura **LVITEM** para retornar as informações solicitadas para o controle. Se o manipulador de mensagens definir o \_ sinalizador LVIF di \_ SETITEM no membro **Mask** da estrutura **LVITEM** , o controle List-View armazenará as informações solicitadas e não solicitará novamente.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

O receptor de notificação converte *lParam* para recuperar a estrutura [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) . O parâmetro *wParam* contém o código de notificação.

Um controle de exibição de lista envia o código de notificação **LVN \_ GETDISPINFO** para recuperar informações de item armazenadas pelo aplicativo em vez do controle. As informações podem ser informações de texto ou ícone de um item. Ele também pode ser informações de estado do item. Consulte a mensagem [**LVM \_ SETCALLBACKMASK**](lvm-setcallbackmask.md) para obter mais informações sobre como implementar o estado do item em uma base de retorno de chamada.

Para obter mais informações sobre retornos de chamada de exibição de lista, consulte [itens de retorno de chamada e a máscara de retorno de chamada](list-view-controls-overview.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra como esse código de notificação pode ser tratado para definir o texto nas colunas de uma exibição de lista. Os dados de cada item são mantidos na estrutura a seguir.


```C++
 typedef struct tagPETINFO
{
    TCHAR szName[50];
    TCHAR szBreed[50];
    TCHAR szGender[7];
    TCHAR szPrice[20];
    GroupIds iGroup;
} PETINFO;
            
```



O seguinte é do manipulador de \_ notificação do WM no procedimento da caixa de diálogo.


```C++
    case WM_NOTIFY:
        switch (((LPNMHDR) lParam)->code)
        {
        case LVN_GETDISPINFO:
            {
                NMLVDISPINFO* plvdi = (NMLVDISPINFO*)lParam;    
                switch (plvdi->item.iSubItem)
                {
                case 0:
                    // rgPetInfo is an array of PETINFO structures.
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szName;
                    break;

                case 1:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szBreed;
                    break;

                case 2:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szGender;
                    break;

                case 3:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szPrice;
                    break;

                default:
                    break;
                }
                return TRUE;
            }
      // More notifications...
      }
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **LVN \_ GETDISPINFOW** (Unicode) e **LVN \_ GETDISPINFOA** (ANSI)<br/>           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**LVN \_ SETDISPINFO**](lvn-setdispinfo.md)
</dt> </dl>

 

 





