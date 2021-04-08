---
description: A estrutura ENTRYPOINTs define os pontos de entrada para as funções de exportação que Monitor de Rede usa para operar o analisador.
ms.assetid: e2ac118d-e04b-489f-877f-84cc9888f8af
title: Estrutura de ENTRYPOINTs (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ENTRYPOINTS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3eebee878cd907ee20674224a969c82038f4ac6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920713"
---
# <a name="entrypoints-structure"></a>Estrutura de ENTRYPOINTs

A estrutura **entryPoints** define os pontos de entrada para as funções de exportação que monitor de rede usa para operar o analisador.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct __ENTRYPOINTS {
  REGISTER         Register;
  DEREGISTER       Deregister;
  RECOGNIZEFRAME   RecognizeFrame;
  ATTACHPROPERTIES AttachProperties;
  FORMATPROPERTIES FormatProperties;
} ENTRYPOINTS, *LPENTRYPOINTS;
```



## <a name="members"></a>Membros

<dl> <dt>

**Registrar**
</dt> <dd>

Ponteiro para a implementação da função de [*especialista de registro*](register-expert.md) .

</dd> <dt>

**Cancelar registro**
</dt> <dd>

Ponteiro para a implementação da função de [**cancelamento de registro**](deregister.md) .

</dd> <dt>

**RecognizeFrame**
</dt> <dd>

Ponteiro para a implementação da função de exportação [**RecognizeFrame**](recognizeframe.md) .

</dd> <dt>

**Anexarproperties**
</dt> <dd>

Ponteiro para a implementação da função de exportação [**attachproperties**](attachproperties.md) .

</dd> <dt>

**Formatproperties**
</dt> <dd>

Ponteiro para a implementação da função de exportação [**formatproperties**](formatproperties.md) .

</dd> </dl>

## <a name="remarks"></a>Comentários

A função **createprotocol** usa a estrutura **entryPoints** para fornecer ponteiros para monitor de rede. Os ponteiros devem ser especificados na ordem identificada na seção membros anteriores.

A função [**formatproperties**](formatproperties.md) não precisará ser implementada se monitor de rede nunca exibirá os dados do protocolo. Por exemplo, **formatproperties** não precisa ser implementado se um aplicativo de exportação usar a saída do analisador e monitor de rede não exibir a saída.



| Para obter informações sobre                                        | Consulte                                                     |
|-----------------------------------------------------------|---------------------------------------------------------|
| Quais analisadores são e como eles funcionam com Monitor de Rede. | [Analisadores](parsers.md)                                  |
| A implementação de **DllMain**  inclui um exemplo.        | [Implementando DllMain](implementing-dllmain-parser.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Anexarproperties](attachproperties.md)
</dt> <dt>

[Createprotocol](createprotocol.md)
</dt> <dt>

[Cancelar registro](deregister.md)
</dt> <dt>

[Formatproperties](formatproperties.md)
</dt> <dt>

[RecognizeFrame](recognizeframe.md)
</dt> <dt>

[Registrar](register-parser.md)
</dt> </dl>

 

 




