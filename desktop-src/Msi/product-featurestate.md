---
description: A propriedade Featurestate é o estado de instalação do recurso para a instância deste produto. Essa propriedade chama MsiQueryFeatureStateEx, com o ProductCode, userid e o contexto do objeto. A ID do recurso é fornecida como um parâmetro.
ms.assetid: 6821be80-4065-465e-b4c9-4cf17856bc5f
title: Método Product. Featurestate
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.FeatureState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3f7e602ce5d5b0a8e524f76144c7f1eff8876bb5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750222"
---
# <a name="productfeaturestate-method"></a>Método Product. Featurestate

A propriedade **featurestate** é o estado de instalação do recurso para a instância deste produto.

Essa propriedade chama [**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa), com o *ProductCode*, *userid* e o *contexto* do objeto. A ID do recurso é fornecida como um parâmetro.

## <a name="syntax"></a>Sintaxe


```JScript
Product.FeatureState(
  FeatureId
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Recurso de funcionalidade* 
</dt> <dd>

ID do recurso que aparece na coluna recurso da [tabela de recursos](feature-table.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Se a chamada for bem sucedido, a propriedade conterá o valor como um **DWORD**.



| Estado                    | Significado                                      |
|--------------------------|----------------------------------------------|
| INSTALLstate \_ anunciado | Este recurso é anunciado.                  |
| INSTALAR \_ local      | O recurso é instalado localmente.            |
| origem de INSTALLstate \_     | O recurso é instalado para ser executado da origem. |



 

Se a chamada falhar, a propriedade conterá um código de erro de [**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa).



| Erro                     | Significado                                                                                                                                    |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| ERRO de \_ acesso \_ negado     | O processo de chamada deve ter privilégios administrativos para obter informações de um produto instalado para um usuário que não seja o usuário atual. |
| ERRO \_ de \_ configuração incorreta | Os dados de configuração estão corrompidos.                                                                                                         |
| \_parâmetro inválido de erro \_ | Um parâmetro inválido foi passado para a função.                                                                                           |
| êxito do erro \_            | A função foi concluída com êxito.                                                                                                       |
| ERRO \_ desconhecido \_ recurso   | A ID do recurso não identifica um recurso conhecido.                                                                                          |
| ERRO \_ de \_ produto desconhecido   | O código do produto não identifica um produto conhecido.                                                                                        |
| \_falha na função de erro \_   | Uma falha interna inesperada.                                                                                                            |



 

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

[**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa)
</dt> <dt>

[Sem suporte no Windows Installer 2,0 e versões anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




