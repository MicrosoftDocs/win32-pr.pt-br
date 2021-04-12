---
title: Mensagem de HKM_SETRULES (commctrl. h)
description: Define as combinações inválidas e a combinação de modificador padrão para um controle de tecla de acesso.
ms.assetid: de3dd463-a534-4c7c-ae04-da80a3bff2ab
keywords:
- Controles de HKM_SETRULES de mensagens do Windows
topic_type:
- apiref
api_name:
- HKM_SETRULES
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c33c0918a7bb44fdac9a1f2c60fdde8e06b5e679
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455339"
---
# <a name="hkm_setrules-message"></a>\_Mensagem hkm SETrules

Define as combinações inválidas e a combinação de modificador padrão para um controle de tecla de acesso.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Uma matriz de sinalizadores que especificam combinações de chaves inválidas. Esse parâmetro pode ser uma combinação dos seguintes valores:



| Valor                                                                                                                                                   | Significado                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| <span id="HKCOMB_A"></span><span id="hkcomb_a"></span><dl> <dt>**HKCOMB \_ A**</dt> </dl>          | ALT<br/>             |
| <span id="HKCOMB_C"></span><span id="hkcomb_c"></span><dl> <dt>**HKCOMB \_ C**</dt> </dl>          | CTRL<br/>            |
| <span id="HKCOMB_CA"></span><span id="hkcomb_ca"></span><dl> <dt>**\_AC HKCOMB**</dt> </dl>       | CTRL + ALT<br/>        |
| <span id="HKCOMB_NONE"></span><span id="hkcomb_none"></span><dl> <dt>**HKCOMB \_ nenhum**</dt> </dl> | Chaves não modificadas<br/> |
| <span id="HKCOMB_S"></span><span id="hkcomb_s"></span><dl> <dt>**HKCOMB \_ S**</dt> </dl>          | ALTERNÂNCIA<br/>           |
| <span id="HKCOMB_SA"></span><span id="hkcomb_sa"></span><dl> <dt>**\_SA HKCOMB**</dt> </dl>       | SHIFT+ALT<br/>       |
| <span id="HKCOMB_SC"></span><span id="hkcomb_sc"></span><dl> <dt>**HKCOMB \_ SC**</dt> </dl>       | SHIFT + CTRL<br/>      |
| <span id="HKCOMB_SCA"></span><span id="hkcomb_sca"></span><dl> <dt>**HKCOMB \_ SCA**</dt> </dl>    | SHIFT + CTRL + ALT<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Uma matriz de sinalizadores que especificam a combinação de teclas a ser usada quando o usuário insere uma combinação inválida. Para obter uma lista de valores de sinalizador modificadores, consulte a descrição da mensagem [**hkm \_ getteclaize**](hkm-gethotkey.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Quando um usuário insere uma combinação de teclas inválida, conforme definido pelos sinalizadores especificados em *wParam*, o sistema usa o operador bit-a-or para combinar as chaves inseridas pelo usuário com os sinalizadores especificados em *lParam*. A combinação de chave resultante é convertida em uma cadeia de caracteres e, em seguida, exibida no controle de tecla de acesso.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





