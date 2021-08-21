---
title: Métodos de propriedade IADsNameTranslate (IADs. h)
description: Define a propriedade ChaseReferral.
ms.assetid: 7c44fe9b-16a5-4bd5-a80b-8f3dcfec20cc
ms.tgt_platform: multiple
keywords:
- ADSI de métodos de propriedade IADsNameTranslate
topic_type:
- apiref
api_name:
- IADsNameTranslate Property Methods
- IADsNameTranslate.ChaseReferral
- IADsNameTranslate.put_ChaseReferral
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3993c3f3680dca46d2f880705fae44812a3bb5fd7a046084c1d818c3433ea7f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082380"
---
# <a name="iadsnametranslate-property-methods"></a>Métodos de propriedade IADsNameTranslate

O método Property da interface [**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate) define a propriedade **ChaseReferral** . Para obter mais informações, consulte [interface Property Methods](interface-property-methods.md).

## <a name="properties"></a>Propriedades

<dl> <dt>

**ChaseReferral**
</dt> <dd> <dl>

Opções de busca de referência conforme definido em [**anúncios \_ Chase \_ referências \_ enum**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum). Quando a caça de referência é definida, a conversão de nome é executada em objetos que não pertencem a esse diretório e são as indicações retornadas da busca de referência.

<dt>

Tipo de acesso: somente gravação
</dt> <dt>

Tipo de dados de script: **longo**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT put_ChaseReferral(
  [in] LONG lnChaseReferral
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>Comentários

As opções de caça de referência se aplicam somente quando você usa [**IADsNameTranslate:: Set**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-set) e [**IADsNameTranslate:: Get**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-get). O recurso não está disponível com [**IADsNameTranslate:: SetEx**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-setex) ou [**IADsNameTranslate:: GetEx**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-getex).

A interface [**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate) tem uma implementação parcial de [**anúncios \_ Chase \_ indicações de referências \_**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) por meio da propriedade **ChaseReferral** . Se a propriedade **ChaseReferral** for definida como zero (0), será o mesmo que especificar **anúncios \_ Chase \_ referências \_ nunca** (0). Se um valor diferente de zero for usado, ele será o mesmo que especificar **anúncios \_ Chase \_ referências \_ sempre** (0x60). O **IADsNameTranslate** não implementa as opções de **ad \_ Chase \_ \_ subordinadas** (0x20) ou **ADS \_ Chase \_ referências \_ externas** (0x40).

A configuração padrão para a procura de referência está habilitada (o **ADS \_ Chase as \_ referências \_ sempre**). Sem a busca de referência, você pode fazer com que a conversão de nomes seja executada nesses objetos que residem somente no servidor de diretório conectado. Se você não tiver certeza se o objeto de interesse está no servidor especificado, defina essa propriedade como **ADS \_ Chase \_ referências \_ sempre**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsNameTranslate é definido como B1B272A3-3625-11D1-A3A4-00C04FB950DC<br/>    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Enumeração de referências do ADS \_ Chase \_ \_**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum)
</dt> <dt>

[**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate)
</dt> <dt>

[**IADsNameTranslate:: Get**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-get)
</dt> <dt>

[**IADsNameTranslate::GetEx**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-getex)
</dt> <dt>

[**IADsNameTranslate:: Set**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-set)
</dt> <dt>

[**IADsNameTranslate::SetEx**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-setex)
</dt> <dt>

[Métodos de propriedade de interface](interface-property-methods.md)
</dt> </dl>

 

 





