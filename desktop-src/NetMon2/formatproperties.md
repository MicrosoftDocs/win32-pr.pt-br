---
description: A função de exportação FormatProperties formata os dados exibidos no painel de detalhes da Monitor de Rede interface do usuário. Se você quiser exibir dados no painel de detalhes, deverá implementar a função de exportação FormatProperties em todas as DLLs do analisador.
ms.assetid: 78e0b4b9-f19e-41cb-8504-635f3f9ac1ee
title: Função de retorno de chamada FormatProperties (Netmon.h)
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
ms.openlocfilehash: 6bb0bc74a52569edbb922aa93edd27b53106073ffdafa3a6cacc5808aab71eef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012244"
---
# <a name="formatproperties-callback-function"></a>Função de retorno de chamada FormatProperties

A **função de exportação FormatProperties** formata os dados exibidos no painel de detalhes da Monitor de Rede interface do usuário. Se você quiser exibir dados no painel de detalhes, deverá implementar a função de exportação **FormatProperties** em todas as DLLs do analisador.

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

*hFrame* \[ Em\]
</dt> <dd>

Lidar com o quadro que está sendo analisado.

</dd> <dt>

*lpFrame* \[ Em\]
</dt> <dd>

Ponteiro para o primeiro byte de um quadro.

</dd> <dt>

*lpProtocol* \[ Em\]
</dt> <dd>

Ponteiro para o início dos dados de protocolo em um quadro.

</dd> <dt>

*nPropertyInsts* \[ Em\]
</dt> <dd>

Número de [estruturas PROPERTYINST](propertyinst.md) fornecidas *por lpPropInst.*

</dd> <dt>

*lpPropInst* \[ Em\]
</dt> <dd>

Ponteiro para uma matriz de [estruturas PROPERTYINST.](propertyinst.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será **TRUE.**

Se a função não for bem-sucedida, o valor de retorno será **FALSE.**

## <a name="remarks"></a>Comentários

Monitor de Rede chama a **função FormatProperties** para exibir dados no painel de detalhes da Monitor de Rede interface do usuário. Normalmente, **FormatProperties** é chamado para formatar a linha de resumo de um protocolo e, em seguida, para formatar todas as instâncias de propriedade do protocolo dentro de um quadro. No entanto, Monitor de Rede garante o número de vezes que chama **FormatProperties** para um analisador específico.

Durante a implementação da função **FormatProperties,** o analisador chama indiretamente a função [FormatPropertyInstance](formatpropertyinstance.md) para usar o formatador genérico que o Monitor de Rede fornece ou pode chamar um procedimento de formatador personalizado definido pelo analisador. Um dos formatador deve ser chamado para cada estrutura [PROPERTYINST](propertyinst.md) passada para a DLL do analisador no *parâmetro lpPropInst.*



| Para obter informações sobre                                          | Consulte                                                                |
|-------------------------------------------------------------|--------------------------------------------------------------------|
| O que são analisadores e como eles funcionam com Monitor de Rede.   | [Analisadores](parsers.md)                                             |
| Quais pontos de entrada estão incluídos na DLL do analisador.          | [Arquitetura de DLL do analisador](parser-dll-architecture.md)             |
| Como implementar **FormatProperties**  inclui um exemplo. | [Implementando FormatProperties](implementing-formatproperties.md) |
| Como o formatante genérico formatar diferentes tipos de dados.  | [Saída de formatação genérica](generic-formatter-output.md)           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[FormatPropertyInstance](formatpropertyinstance.md)
</dt> <dt>

[Propertyinfo](propertyinfo.md)
</dt> <dt>

[PROPERTYINST](propertyinst.md)
</dt> </dl>

 

 




