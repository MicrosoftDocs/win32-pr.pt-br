---
description: A propriedade Componentstate é o estado de instalação do componente para a instância deste produto. Essa propriedade chama MsiQueryComponentState, com o ProductCode, userid e o contexto do objeto.
ms.assetid: 2939048a-42a5-4ffb-868c-251c0f15e5ed
title: Método Product. Componentstate
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
ms.openlocfilehash: 240a854a899f46bf80703bbd6cfb6b1529848586
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748140"
---
# <a name="productcomponentstate-method"></a>Método Product. Componentstate

A propriedade **componentstate** é o estado de instalação do componente para a instância deste produto.

Essa propriedade chama [**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea), com o ProductCode, userid e o contexto do objeto. O GUID de ID de componente é fornecido como um parâmetro.

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

GUID de código de componente do componente como encontrado na coluna ComponentID da [tabela de componentes](component-table.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Se a chamada for bem sucedido, a propriedade conterá o valor como um **DWORD**.



| Estado                | Significado                                            |
|----------------------|----------------------------------------------------|
| INSTALAR \_ local  | O componente é instalado localmente.                |
| origem de INSTALLstate \_ | O componente é instalado para ser executado da origem. |



 

Se a chamada falhar, a propriedade conterá um código de erro de [**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea).



| Erro                     | Significado                                                                                                            |
|---------------------------|--------------------------------------------------------------------------------------------------------------------|
| ERRO de \_ acesso \_ negado     | O processo de chamada deve ter privilégios administrativos para obter informações para um usuário que não seja o usuário atual. |
| ERRO \_ de \_ configuração incorreta | Os dados de configuração estão corrompidos.                                                                                 |
| \_parâmetro inválido de erro \_ | Um parâmetro inválido foi passado para a função.                                                                   |
| êxito do erro \_            | A função foi concluída com êxito.                                                                               |
| ERRO \_ de \_ componente desconhecido | A ID do componente não identifica um componente conhecido.                                                              |
| ERRO \_ de \_ produto desconhecido   | O código do produto não identifica um produto conhecido.                                                                |
| \_falha na função de erro \_   | Uma falha interna inesperada.                                                                                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer 3,0 ou posterior no Windows Server 2003, Windows XP e Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IProduct é definido como 000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Remessa**](product-object.md)
</dt> <dt>

[**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea)
</dt> <dt>

[Sem suporte no Windows Installer 2,0 e versões anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




