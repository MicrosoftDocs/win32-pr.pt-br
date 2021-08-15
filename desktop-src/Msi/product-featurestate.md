---
description: A propriedade FeatureState é o estado de instalação do recurso para a instância deste produto. Essa propriedade chama MsiQueryFeatureStateEx, com ProductCode, UserSid e Context do objeto . A ID do recurso é fornecida como um parâmetro.
ms.assetid: 6821be80-4065-465e-b4c9-4cf17856bc5f
title: Método Product.FeatureState
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
ms.openlocfilehash: 484b8f7f3094cf5bca2cb9d03941d68619995ba98de08e2845c3717439709e2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129046"
---
# <a name="productfeaturestate-method"></a>Método Product.FeatureState

A **propriedade FeatureState** é o estado de instalação do recurso para a instância deste produto.

Essa propriedade chama [**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa), com *ProductCode,* *UserSid* *e Context* do objeto . A ID do recurso é fornecida como um parâmetro.

## <a name="syntax"></a>Sintaxe


```JScript
Product.FeatureState(
  FeatureId
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Featureid* 
</dt> <dd>

ID do recurso que aparece na coluna Recurso da [Tabela de Recursos](feature-table.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Se a chamada for bem-sucedida, a propriedade conterá o valor como **um DWORD.**



| Estado                    | Significado                                      |
|--------------------------|----------------------------------------------|
| INSTALLSTATE \_ ANUNCIADO | Esse recurso é anunciado.                  |
| INSTALLSTATE \_ LOCAL      | O recurso é instalado localmente.            |
| INSTALLSTATE \_ SOURCE     | O recurso é instalado para ser executado da origem. |



 

Se a chamada falhar, a propriedade conterá um código de erro [**de MsiQueryFeatureStateEx.**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa)



| Erro                     | Significado                                                                                                                                    |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| ACESSO \_ DE ERRO \_ NEGADO     | O processo de chamada deve ter privilégios administrativos para obter informações de um produto instalado para um usuário diferente do usuário atual. |
| ERRO \_ DE CONFIGURAÇÃO \_ RUIM | Os dados de configuração estão corrompidos.                                                                                                         |
| ERRO \_ PARÂMETRO \_ INVÁLIDO | Um parâmetro inválido foi passado para a função.                                                                                           |
| ÊXITO \_ DO ERRO            | A função foi concluída com êxito.                                                                                                       |
| RECURSO \_ DE ERRO \_ DESCONHECIDO   | A ID do recurso não identifica um recurso conhecido.                                                                                          |
| ERRO \_ PRODUTO \_ DESCONHECIDO   | O código do produto não identifica um produto conhecido.                                                                                        |
| FALHA \_ NA FUNÇÃO DE \_ ERRO   | Uma falha interna inesperada.                                                                                                            |



 

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

[**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa)
</dt> <dt>

[Sem suporte no Windows 2.0 e versões anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




