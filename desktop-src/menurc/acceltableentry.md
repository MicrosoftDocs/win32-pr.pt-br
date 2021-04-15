---
title: Estrutura ACCELTABLEENTRY
description: Descreve os dados em um recurso de tabela de acelerador individual. A definição de estrutura fornecida aqui é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.
ms.assetid: 510594ae-56ea-49fb-abd3-ec06e51f2e0e
keywords:
- Menus de estrutura ACCELTABLEENTRY e outros recursos
topic_type:
- apiref
api_name:
- ACCELTABLEENTRY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9ff12fe39f2ea54c90530133263bceb157d79dcf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455935"
---
# <a name="acceltableentry-structure"></a>Estrutura ACCELTABLEENTRY

Descreve os dados em um recurso de tabela de acelerador individual. A definição de estrutura fornecida aqui é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  WORD fFlags;
  WORD wAnsi;
  WORD wId;
  WORD padding;
} ACCELTABLEENTRY;
```



## <a name="members"></a>Membros

<dl> <dt>

**fFlags**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Descreve as características do acelerador de teclado. Esse membro pode ter um ou mais dos seguintes valores de WinUser. h.



| Valor                                                                                                                                                                                                      | Significado                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FVIRTKEY"></span><span id="fvirtkey"></span><dl> <dt>**FVIRTKEY**</dt> <dt>true</dt> </dl>    | A chave do acelerador é um [código de chave virtual](/windows/desktop/inputdev/virtual-key-codes). Se esse sinalizador não for especificado, a tecla aceleradora será considerada para especificar um código de caractere ASCII. <br/>                          |
| <span id="FNOINVERT"></span><span id="fnoinvert"></span><dl> <dt>**FNOINVERT**</dt> <dt>0x02</dt> </dl> | Um item de menu na barra de menus não é realçado quando um acelerador é usado. Este atributo é obsoleto e mantido somente para compatibilidade com versões anteriores com arquivos de recursos projetados para o Windows de 16 bits.<br/> |
| <span id="FSHIFT"></span><span id="fshift"></span><dl> <dt>**FSHIFT**</dt> <dt>0x04</dt> </dl>          | O acelerador será ativado somente se o usuário pressionar a tecla SHIFT. Esse sinalizador se aplica somente a chaves virtuais. <br/>                                                                                        |
| <span id="FCONTROL"></span><span id="fcontrol"></span><dl> <dt>**FCONTROL**</dt> <dt>0x08</dt> </dl>    | O acelerador será ativado somente se o usuário pressionar a tecla CTRL. Esse sinalizador se aplica somente a chaves virtuais. <br/>                                                                                         |
| <span id="FALT"></span><span id="falt"></span><dl> <dt>**FALT**</dt> <dt>0x10</dt> </dl>                | O acelerador será ativado somente se o usuário pressionar a tecla ALT. Esse sinalizador se aplica somente a chaves virtuais. <br/>                                                                                          |
| <span id="0x80"></span><span id="0X80"></span><dl> <dt>**0x80**</dt> </dl>                                                                          | A entrada é a última em uma tabela de acelerador. <br/>                                                                                                                                                          |



 

</dd> <dt>

**wAnsi**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Um valor de caractere ANSI ou um código de chave virtual que identifica a chave do acelerador.

</dd> <dt>

**wId**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Um identificador para o acelerador de teclado. Esse é o valor passado para o procedimento de janela quando o usuário pressiona a tecla especificada.

</dd> <dt>

**padding**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

O número de bytes inseridos para garantir que a estrutura seja alinhada em um limite **DWORD** .

</dd> </dl>

## <a name="remarks"></a>Comentários

A estrutura **ACCELTABLEENTRY** é repetida para todas as entradas de tabela de acelerador no recurso. A última entrada na tabela é sinalizada com o valor 0x0080.

Você pode calcular o número de elementos na tabela se dividir o comprimento do recurso em oito. Em seguida, seu aplicativo pode acessar aleatoriamente as entradas individuais de comprimento fixo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**CreateAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Recursos](resources.md)
</dt> </dl>

 

