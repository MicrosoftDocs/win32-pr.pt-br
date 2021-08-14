---
description: A propriedade ComponentState é o estado de instalação do componente para a instância deste produto. Essa propriedade chama MsiQueryComponentState, com ProductCode, UserSid e Context do objeto .
ms.assetid: 2939048a-42a5-4ffb-868c-251c0f15e5ed
title: Método Product.ComponentState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.ComponentState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d2bc9c5c1f5325dc631f8866ba1a8c7d88ce18d624a2974974f4692bf4f7b067
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118376775"
---
# <a name="productcomponentstate-method"></a>Método Product.ComponentState

A **propriedade ComponentState** é o estado de instalação do componente para a instância deste produto.

Essa propriedade chama [**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea), com ProductCode, UserSid e Context do objeto . O GUID de ID do componente é fornecido como um parâmetro.

## <a name="syntax"></a>Sintaxe


```JScript
Product.ComponentState(
  ID
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ID* 
</dt> <dd>

GUID de código do componente, conforme encontrado na coluna ComponentID da [tabela Component](component-table.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Se a chamada for bem-sucedida, a propriedade conterá o valor como **um DWORD.**



| Estado                | Significado                                            |
|----------------------|----------------------------------------------------|
| INSTALLSTATE \_ LOCAL  | O componente é instalado localmente.                |
| INSTALLSTATE \_ SOURCE | O componente é instalado para ser executado da origem. |



 

Se a chamada falhar, a propriedade conterá um código de erro [**de MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea).



| Erro                     | Significado                                                                                                            |
|---------------------------|--------------------------------------------------------------------------------------------------------------------|
| ACESSO \_ DE ERRO \_ NEGADO     | O processo de chamada deve ter privilégios administrativos para obter informações para um usuário diferente do usuário atual. |
| ERRO \_ DE CONFIGURAÇÃO \_ RUIM | Os dados de configuração estão corrompidos.                                                                                 |
| ERRO \_ PARÂMETRO \_ INVÁLIDO | Um parâmetro inválido foi passado para a função.                                                                   |
| ÊXITO \_ DO ERRO            | A função foi concluída com êxito.                                                                               |
| ERRO \_ COMPONENTE \_ DESCONHECIDO | A ID do componente não identifica um componente conhecido.                                                              |
| ERRO \_ PRODUTO \_ DESCONHECIDO   | O código do produto não identifica um produto conhecido.                                                                |
| FALHA \_ NA FUNÇÃO DE \_ ERRO   | Uma falha interna inesperada.                                                                                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador 3.0 ou posterior no Windows Server 2003, Windows XP e Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID IProduct é definido como \_ 000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Produto**](product-object.md)
</dt> <dt>

[**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea)
</dt> <dt>

[Sem suporte no Windows 2.0 e versões anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




