---
description: A função Formatproperties Export formata os dados que são exibidos no painel de detalhes da interface do usuário do Monitor de Rede. Se você quiser exibir dados no painel de detalhes, deverá implementar a função Formatproperties Export em todas as DLLs do analisador.
ms.assetid: 78e0b4b9-f19e-41cb-8504-635f3f9ac1ee
title: Função de retorno de chamada formatproperties (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FormatProperties
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 61707b49fa88490e1aa22ac89f33dfd97ec20cbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753428"
---
# <a name="formatproperties-callback-function"></a>Função de retorno de chamada formatproperties

A função **formatproperties** Export formata os dados que são exibidos no painel de detalhes da interface do usuário do monitor de rede. Se você quiser exibir dados no painel de detalhes, deverá implementar a função **formatproperties** Export em todas as DLLs do analisador.

## <a name="syntax"></a>Sintaxe


```C++
DWORD FormatProperties(
  _In_ HFRAME         hFrame,
  _In_ LPBYTE         lpFrame,
  _In_ LPBYTE         lpProtocol,
  _In_ DWORD          nPropertyInsts,
  _In_ LPPROPERTYINST lpPropInst
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hFrame* \[ no\]
</dt> <dd>

Identificador para o quadro que está sendo analisado.

</dd> <dt>

*lpFrame* \[ no\]
</dt> <dd>

Ponteiro para o primeiro byte de um quadro.

</dd> <dt>

*lpProtocol* \[ no\]
</dt> <dd>

Ponteiro para o início dos dados de protocolo em um quadro.

</dd> <dt>

*nPropertyInsts* \[ no\]
</dt> <dd>

Número de estruturas [PROPERTYINST](propertyinst.md) fornecidas por *lpPropInst*.

</dd> <dt>

*lpPropInst* \[ no\]
</dt> <dd>

Ponteiro para uma matriz de estruturas [PROPERTYINST](propertyinst.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será **true**.

Se a função não for bem-sucedida, o valor de retorno será **false**.

## <a name="remarks"></a>Comentários

Monitor de Rede chama a função **formatproperties** para exibir dados no painel de detalhes da interface do usuário do monitor de rede. Normalmente, **formatproperties** é chamado para formatar a linha de Resumo de um protocolo e, em seguida, Formatar todas as instâncias de Propriedade do protocolo dentro de um quadro. No entanto, Monitor de Rede não garante o número de vezes que ele chama **formatproperties** para um analisador específico.

Durante a implementação da função **formatproperties** , o analisador indiretamente chama a função [FormatPropertyInstance](formatpropertyinstance.md) para usar o formatador genérico que o monitor de rede fornece, ou pode chamar um procedimento formatador personalizado que é definido pelo analisador. Um dos formatadores deve ser chamado para cada estrutura [PROPERTYINST](propertyinst.md) passada para a DLL do analisador no parâmetro *lpPropInst* .



| Para obter informações sobre                                          | Consulte                                                                |
|-------------------------------------------------------------|--------------------------------------------------------------------|
| Quais analisadores são e como eles funcionam com Monitor de Rede.   | [Analisadores](parsers.md)                                             |
| Quais pontos de entrada são incluídos na DLL do analisador.          | [Arquitetura de DLL do analisador](parser-dll-architecture.md)             |
| Como implementar **formatproperties**  inclui um exemplo. | [Implementando Formatproperties](implementing-formatproperties.md) |
| Como o formatador genérico formata diferentes tipos de dados.  | [Saída de formatador genérico](generic-formatter-output.md)           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[FormatPropertyInstance](formatpropertyinstance.md)
</dt> <dt>

[PROPERTYINFO](propertyinfo.md)
</dt> <dt>

[PROPERTYINST](propertyinst.md)
</dt> </dl>

 

 




